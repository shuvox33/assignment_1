Answer of question number 2:

TypeScript এ keyof কোনো অবজেক্ট টাইপের সবগুলো key কে union টাইপ হিসেবে রিটার্ন করে।
অর্থাৎ, এটি আমাদেরকে অবজেক্টের key-গুলোকে টাইপ হিসেবে ব্যবহার করতে সাহায্য করে।

Example:

type User = {
name: string;
age: number;
email: string;
};

type UserKeys = keyof User;

function getUserProperty(user: User, key: UserKeys) {
return user[key];
}

const person: User = {
name: "Shakib",
age: 25,
email: "shakib@test.com",
};

console.log(getUserProperty(person, "email"));

Answer of question number 4:

Union Type : Union টাইপ মানে হলো একটি ভ্যারিয়েবল একাধিক টাইপের যেকোনো একটির হতে পারে।

Example:

function printValue(value: string | number) {
console.log("Value:", value);
}

printValue("Hello");
printValue(123);

Intersection Type : Intersection টাইপ মানে হলো একাধিক টাইপকে মিলিয়ে একটি টাইপ তৈরি করা, এবং সেই নতুন টাইপে সবগুলোর প্রপার্টি থাকতে হবে।

Example:

type Address = {
city: string;
};

type FullUser = Name & Age & Address;

const fullInfo: FullUser = {
name: "Arif",
age: 30,
city: "Dhaka",
};
