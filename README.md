# interface এবং type এর মধ্যে পার্থক্য

- interface দিয়ে number, string, boolean এর মতো primitive type বানানো যায় না। কিন্তু type দিয়ে করা যায়।

- একই নামের interface বারবার লিখলে তারা merge হয়ে যায়। কিন্তু type হয় না

- Union (|) interface এ ব্যবহার করা যায় না । কিন্তু type এ করা যায়

- Intersection (&) interface এ ব্যবহার করা যায় না । কিন্তু type এ করা যায় ।

# Union এবং Intersection উদাহরণ

## Union Type (|)

```ts
type Id = string | number;
const printId = (id: Id) => {
  console.log("ID: ", id);
};

printId(353656);
```

## Intersection (&)

```ts
type Student = {
  name: string;
};

type results = {
  CGPA: number;
};

type student_info = Student & results;

const student1: student_info = {
  name: "Hero Alom",
  CGPA: 2.99,
};
```
