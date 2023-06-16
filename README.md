<p align="center"><a href="https://xxai.art"><img src="https://cdn.jsdelivr.net/gh/xxai-art/doc/logo.svg"/></a><br/><a href="https://xxai.art"><img src="https://cdn.jsdelivr.net/gh/xxai-art/doc/xxai.svg"/></a></p><p align="center"><a href="https://github.com/xxai-art/doc#readme"><img alt="I18N" src="https://cdn.jsdelivr.net/gh/wactax/img/t.svg"/></a>　<a href="https://groups.google.com/u/0/g/xxai-art"><img alt="Google Groups" src="https://cdn.jsdelivr.net/gh/wactax/img/g-groups.svg"/></a></p>

# xxAI.art

ওয়েবসাইট কোডের অংশ ওপেন সোর্স, অনুবাদ অপ্টিমাইজ করতে সাহায্য করার জন্য স্বাগতম।

## ফ্রন্ট-এন্ড কোড

* [ফ্রন্ট-এন্ড কোড](https://github.com/xxai-art/web)
* [সমগ্র সাইটের জন্য ভাষা প্যাক](https://github.com/xxai-art/web/tree/main/i18n)
* [লগইন মডিউলগুলির জন্য ভাষা প্যাক](https://github.com/wacpkg/user/tree/main/ui.i18n)
* [ওয়েবসাইট বহুভাষিক ডকুমেন্টেশন](https://github.com/xxai-doc)

ফ্রন্ট-এন্ড প্রোগ্রামিং ভাষা হল [@w5/coffee_plus](http://npmjs.com/@w5/coffee_plus) , যা কফিস্ক্রিপ্ট সিনট্যাক্সের উপর ভিত্তি করে কিছু বৈশিষ্ট্য যুক্ত করে, দেখুন [./coffee_plus.md](./coffee_plus.md) ।

## ওয়েবসাইট এবং নথির আন্তর্জাতিকীকরণ

নিম্নলিখিত 3টি প্রকল্পের উপর তৈরি করুন

* [@w5/mdt](https://www.npmjs.com/package/@w5/mdt)

  প্রত্যয়টি হল `.mdt` , আপনি বাহ্যিক ফাইলগুলিকে উল্লেখ করতে `<+ ./coffee_plus/import.js>` এর অনুরূপ সিনট্যাক্স ব্যবহার করতে পারেন এবং `.md` প্রত্যয় দিয়ে মার্কডাউন তৈরি করতে পারেন।

* [@w5/trmd](https://www.npmjs.com/package/@w5/trmd)

  মার্কডাউন অনুবাদ কোড এবং লিঙ্কগুলিকে অনুবাদ করবে না এবং অনুবাদিত বাক্যগুলি ক্যাশে করবে৷ যদি অনুবাদটি পরিবর্তন করা হয় কিন্তু মূল পাঠ্যটি পরিবর্তিত না হয়, তাহলে এটিকে আবার সম্পাদন করলে অনুবাদের পরিবর্তনটি ওভাররাইট হবে না।

* [@w5/i18n](https://www.npmjs.com/package/@w5/i18n)

  `yaml` জেনারেট করা ওয়েবসাইটগুলি অনুবাদ করার জন্য ভাষা ফাইল।

### নথি অনুবাদ অটোমেশন নির্দেশাবলী

রিপোজিটরি [xxai-art/doc](https://github.com/xxai-art/doc) দেখুন

প্রথমে nodejs, [direnv](https://direnv.net) এবং [bun](https://github.com/oven-sh/bun) ইনস্টল করার পরামর্শ দেওয়া হয় এবং তারপর ডিরেক্টরিতে প্রবেশ করার পরে `direnv allow` চালান।

শত শত ভাষায় অনূদিত অত্যধিক বড় গুদামগুলি এড়াতে, আমি প্রতিটি ভাষার জন্য একটি পৃথক কোড গুদাম তৈরি করেছি এবং এই গুদামটি সংরক্ষণ করার জন্য একটি সংস্থা তৈরি করেছি

পরিবেশ পরিবর্তনশীল `GITHUB_ACCESS_TOKEN` সেট করা এবং তারপর [create.github.coffee](https://github.com/xxai-art/doc/blob/main/create.github.coffee) চালানো স্বয়ংক্রিয়ভাবে গুদাম তৈরি করবে।

অবশ্যই, আপনি এটি একটি গুদামেও রাখতে পারেন।

অনুবাদ স্ক্রিপ্ট রেফারেন্স [run.sh](https://github.com/xxai-art/doc/blob/main/run.sh)

স্ক্রিপ্ট কোড নিম্নরূপ ব্যাখ্যা করা হয়:

[bunx](https://bun.sh/docs/cli/bunx) হল npx এর প্রতিস্থাপন, যা দ্রুততর। অবশ্যই, যদি আপনার বান ইনস্টল না থাকে তবে আপনি পরিবর্তে `npx` ব্যবহার করতে পারেন।

`bunx mdt zh` `.mdt` `.md` হিসাবে zh ডিরেক্টরিতে রেন্ডার করে, নীচের লিঙ্ক করা 2টি ফাইল দেখুন

* [coffee_plus.mdt](https://github.com/xxai-doc/zh/blob/main/coffee_plus.mdt)
* [coffee_plus.md](https://github.com/xxai-doc/zh/blob/main/coffee_plus.md)

`bunx i18n` হল অনুবাদের মূল কোড (যদি আপনার শুধুমাত্র `nodejs` ইনস্টল করা থাকে, কিন্তু `bun` এবং `direnv` ইনস্টল করা না থাকে, তাহলে আপনি অনুবাদ করতে `npx i18n` চালাতে পারেন)।

এটি [i18n.yml](https://github.com/xxai-art/doc/blob/main/i18n.yml) পার্স করবে, এই নথিতে `i18n.yml` এর কনফিগারেশন নিম্নরূপ:

```
en:
zh: ja ko en
```

অর্থ হল: চীনা অনুবাদ জাপানি, কোরিয়ান, ইংরেজি, অন্যান্য সমস্ত ভাষায় ইংরেজি অনুবাদ। আপনি যদি শুধুমাত্র চীনা এবং ইংরেজি সমর্থন করতে চান, আপনি শুধু `zh: en` লিখতে পারেন।

শেষটি হল [gen.README.coffee](https://github.com/xxai-art/doc/blob/main/gen.README.coffee) , যা মূল শিরোনাম এবং প্রতিটি ভাষার `README.md` এর প্রথম সাবটাইটেলের মধ্যে বিষয়বস্তু বের করে `README.md` এন্ট্রি তৈরি করে। কোডটি খুবই সহজ, আপনি নিজেই এটি দেখতে পারেন।

Google API বিনামূল্যে অনুবাদের জন্য ব্যবহার করা হয়। আপনি যদি Google অ্যাক্সেস করতে না পারেন, অনুগ্রহ করে কনফিগার করুন এবং একটি প্রক্সি সেট করুন, যেমন:

```
export https_proxy=http://127.0.0.1:7890 http_proxy=http://127.0.0.1:7890 all_proxy=socks5://127.0.0.1:7890
```

অনুবাদ স্ক্রিপ্টটি `.i18n` ডিরেক্টরিতে একটি অনুবাদ ক্যাশে তৈরি করবে, অনুগ্রহ করে এটিকে `git status` দিয়ে পরীক্ষা করুন এবং বারবার অনুবাদ এড়াতে কোড সংগ্রহস্থলে যোগ করুন।
