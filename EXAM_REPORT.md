# Git პრაქტიკული გამოცდის ანგარიში

## I ეტაპი — ლოკალური რეპოზიტორია
- შექმნილია `exam-project`-ის ეკვივალენტური დამოუკიდებელი პროექტი `SkillWill_Git_Exam`.
- Git ინიციალიზებულია `main` branch-ით.
- საწყისი `index.html`, `README.md` და `.gitignore` დაემატა პირველ commit-ში.

## II ეტაპი — Branch და merge
- შეიქმნა `feature-header` განშტოება.
- `index.html`-ში დაემატა „ჩვენ შესახებ“ ბმული.
- ცვლილება დაკომიტდა და შერწყმულია `main`-თან.

## III ეტაპი — Merge conflict
- `nav-feature` განშტოებაში `<nav>` ხაზს დაემატა „კურსები“.
- `nav-alt` განშტოებაში იმავე ხაზს დაემატა „კონტაქტი“.
- `nav-feature` შეერწყა `main`-ს, `nav-alt` merge-მა გამოიწვია რეალური Git `CONFLICT (content)`.
- `index.html`-ში კონფლიქტის მარკერები `<<<<<<<`, `=======`, `>>>>>>>` წაიშალა და ორივე ცვლილება შენარჩუნდა.
- დასრულდა merge commit-ით.

## შესამოწმებელი ბრძანებები
```bash
git status
git log --oneline --graph --all --decorate
git branch -a
```

## GitHub-ზე ატვირთვა (საჭირო ნაბიჯი)
ადგილობრივი Git ისტორია შექმნილია, მაგრამ ამ არქივისთვის რეალურ GitHub remote-ზე push **არ შესრულებულა**.

1. შედი GitHub-ში და შექმენი ცარიელი public ან private repository სახელად `SkillWill_Git_Exam` (README-ის ავტომატური შექმნის გარეშე).
2. გახსენი ეს საქაღალდე VS Code-ში.
3. ტერმინალში ჩაწერე:
```bash
git remote add origin https://github.com/YOUR_USERNAME/SkillWill_Git_Exam.git
git push -u origin main
git push origin feature-header nav-feature nav-alt
```
`YOUR_USERNAME` ჩაანაცვლე შენი რეალური GitHub მომხმარებლის სახელით. საჭიროების შემთხვევაში შედი GitHub-ის ავტორიზაციაში. ნუ ჩაამატებ პაროლებს, token-ებს ან credentials-ს პროექტის ფაილებში.

**შენიშვნა:** ლოკალური დემონსტრაციის commit-ების ავტორად მითითებულია `SkillWill Exam Student <student@example.invalid>`, რადგან რეალური Git email არ ყოფილა მოცემული. თუ მასწავლებელი მოითხოვს პერსონალური ავტორით commit-ებს, მათი იდენტიფიკაცია უნდა გადაამოწმო Git-ის პარამეტრებში.
