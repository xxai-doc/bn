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
