<script setup lang="ts">
import { ref } from "vue";
import CtaButton from "./components/CtaButton.vue";

const outcomes = [
  {
    n: "01",
    title: "Власний інвестиційний мандат",
    text: "Документ на одну сторінку, який відповість, у що ви інвестуєте, а у що принципово ні.",
  },
  {
    n: "02",
    title: "Розмір позиції без «на відчуття»",
    text: "Навчитесь рахувати розмір позиції за чіткими лімітами ризику.",
  },
  {
    n: "03",
    title: "Стрес-тест портфеля",
    text: "Побачите слабкі місця свого портфеля до того, як їх покаже ринок — з готовим планом дій на кожен сценарій.",
  },
  {
    n: "04",
    title: "Власний паттерн помилок",
    text: "Дізнаєтесь, де систематично переоцінюєте чи недооцінюєте свою впевненість — і зможете це виправити.",
  },
  {
    n: "05",
    title: "Виміряний прогрес",
    text: "Порівняєте своє рішення «до» і «після» курсу на одному й тому ж кейсі — не повіримо на слово.",
  },
];

const audience = [
  "Ви пройшли «Основи інвестування» і/або «Інвестування у фондовий ринок» і знаєте базові поняття",
  "Ви знаєте багато термінів, але досі не впевнені у власних рішеннях з капіталом",
  "Ви хочете не ще теорії, а чітку систему: мандат, оцінка ідей, розмір позиції, управління портфелем",
  "Ви готові письмово фіксувати свої рішення й чесно аналізувати власні помилки — саме на цьому тримається метод курсу",
];

const benefits = [
  {
    n: "01",
    title: "Дізнаєтесь першими",
    text: "Коли відкриються продажі й на яких умовах — ще до публічного анонсу.",
  },
  {
    n: "02",
    title: "Гарантоване місце",
    text: "100% гарантоване місце в першому потоці курсу.",
  },
  {
    n: "03",
    title: "Найкраща ціна",
    text: "Найкраща з усіх, що будуть — зв'яжемося з вами особисто, щойно вона буде фінально затверджена.",
  },
];

const faqs = [
  {
    q: "Я вже проходив два курси, навіщо мені ще один?",
    a: "Курс не додає ще теми, а перебудовує вже відомий матеріал навколо конкретних рішень: не «знати більше», а «судити краще».",
  },
  {
    q: "Це знову просто теорія?",
    a: "Кожна тема закінчується історичним кейсом із фіксацією рішення до розкриття результату. 10 кейсів і 4 робочі документи — не конспект, а особиста операційна модель.",
  },
  {
    q: "Скільки коштуватиме курс?",
    a: "Фінальну ціну ми оголосимо особисто тим, хто зареєструвався на передзапис, — і саме вони отримають найкращу ціну з усіх, що будуть. Що раніше залишите заявку, то раніше дізнаєтесь умови.",
  },
  {
    q: "Заповнюючи анкету, я вже плачу?",
    a: "Ні. Анкета — це бронювання місця й найкращої ціни, а не оплата. Ми зв'яжемося з вами особисто, щоб завершити реєстрацію й оплату.",
  },
];

const priorOptions = ["Так", "Частково", "Ні"];

const sent = ref(false);
const prior = ref("");

function handleSubmit() {
  sent.value = true;
}
</script>

<template>
  <div class="min-h-screen bg-background font-sans text-foreground">
    <!-- Header -->
    <header class="mx-auto flex max-w-6xl items-center justify-between px-5 py-5 sm:px-8">
      <a href="/" class="flex items-center gap-2.5">
        <span class="text-2xl font-black leading-none text-accent select-none">V</span>
        <span class="text-[0.8125rem] font-bold leading-[1.15] tracking-tight text-foreground">
          школа<br />останнього капіталіста
        </span>
      </a>
      <a
        href="#forma"
        class="rounded-xl border border-primary px-5 py-2.5 text-sm font-bold text-primary transition-colors hover:bg-primary hover:text-primary-foreground"
      >
        Залишити заявку
      </a>
    </header>

    <!-- Hero -->
    <section class="mx-auto max-w-6xl px-5 pb-24 pt-14 sm:px-8 sm:pt-24">
      <div class="flex items-center gap-3">
        <span
          class="rise-in inline-flex rotate-[-3deg] rounded-lg bg-primary px-3 py-1.5 text-sm font-extrabold text-primary-foreground"
        >
          🆕 Новий курс
        </span>
      </div>
      <h1 class="mt-8 font-display text-5xl font-extrabold leading-[1.02] tracking-tight sm:text-7xl">
        Просунуте <mark class="mark-accent-hero">інвестування</mark>
      </h1>
      <p class="mt-8 max-w-2xl text-base leading-relaxed text-muted-foreground sm:text-lg">
        Особиста система прийняття інвестиційних рішень — інвестиційний мандат,
        оцінка ідей, розмір позиції, стрес-тест портфеля — яку ви застосовуєте до
        власних грошей вже під час курсу, а не в теорії.
      </p>
      <div class="mt-10 flex flex-wrap items-center gap-5">
        <CtaButton />
        <span class="text-sm text-muted-foreground">
          Передзапис відкритий до <span class="font-bold text-primary">15.09</span>
        </span>
      </div>
    </section>

    <!-- Outcomes — light section -->
    <section class="rounded-t-[2.5rem] bg-paper py-20 text-paper-foreground sm:py-28">
      <div class="mx-auto max-w-6xl px-5 sm:px-8">
        <h2 class="max-w-md font-display text-4xl font-extrabold leading-tight tracking-tight sm:text-5xl">
          Результати курсу
        </h2>
        <p class="mt-6 max-w-2xl text-base leading-relaxed text-paper-muted">
          Це не поглиблення базових курсів — це наступний рівень: там ви отримали
          знання й термінологію, тут — систему, яку одразу застосовуєте до власного
          портфеля.
        </p>

        <div class="mt-14 grid gap-x-10 gap-y-12 sm:grid-cols-2 lg:grid-cols-3">
          <div v-for="o in outcomes" :key="o.n" class="border-t border-paper-foreground/15 pt-5">
            <span class="text-lg font-extrabold text-lime-soft">{{ o.n }}</span>
            <h3 class="mt-4 font-display text-2xl font-bold leading-snug">{{ o.title }}</h3>
            <p class="mt-3 text-sm leading-relaxed text-paper-muted">{{ o.text }}</p>
          </div>
        </div>
      </div>
    </section>

    <!-- Audience -->
    <section class="rounded-t-[2.5rem] bg-background py-20 sm:py-28">
      <div class="mx-auto grid max-w-6xl gap-12 px-5 sm:px-8 lg:grid-cols-2">
        <div>
          <h2 class="font-display text-4xl font-extrabold leading-tight tracking-tight sm:text-5xl">
            Для кого цей <mark class="mark-accent">курс</mark>
          </h2>
        </div>
        <ul class="space-y-5">
          <li v-for="item in audience" :key="item" class="flex gap-4 text-base leading-relaxed">
            <span
              class="mt-1 grid size-6 shrink-0 place-items-center rounded-full bg-primary/15 text-xs font-extrabold text-primary"
            >
              ✓
            </span>
            {{ item }}
          </li>
        </ul>
      </div>
      <div class="mx-auto mt-14 max-w-6xl px-5 sm:px-8">
        <div class="rounded-2xl bg-surface p-6 sm:p-8">
          <p class="text-sm font-bold uppercase tracking-widest text-accent">Курс не для тих, хто</p>
          <p class="mt-3 max-w-4xl text-base leading-relaxed text-muted-foreground">
            Хоче стати професійним аналітиком акцій чи портфельним менеджером, і не для
            тих, хто чекає точного прогнозу ринку — «Просунуте інвестування» вчить
            працювати з невизначеністю, а не усувати її.
          </p>
        </div>
      </div>
    </section>

    <!-- Benefits -->
    <section class="mx-auto max-w-6xl px-5 pb-20 sm:px-8 sm:pb-28">
      <h2 class="font-display text-4xl font-extrabold leading-tight tracking-tight sm:text-5xl">
        Що дає <mark class="mark-accent">передзапис</mark>
      </h2>
      <div class="mt-12 grid gap-4 md:grid-cols-3">
        <div v-for="b in benefits" :key="b.n" class="rounded-2xl bg-surface p-7">
          <span class="text-3xl font-extrabold text-primary">{{ b.n }}</span>
          <h3 class="mt-5 font-display text-xl font-bold">{{ b.title }}</h3>
          <p class="mt-2 text-sm leading-relaxed text-muted-foreground">{{ b.text }}</p>
        </div>
      </div>
    </section>

    <!-- Form -->
    <section id="forma" class="mx-auto max-w-6xl px-5 pb-24 sm:px-8">
      <div class="grid gap-12 rounded-[2rem] bg-surface p-7 sm:p-12 lg:grid-cols-2">
        <div>
          <h2 class="font-display text-3xl font-extrabold leading-tight tracking-tight sm:text-4xl">
            Залишити заявку на <mark class="mark-accent">передзапис</mark>
          </h2>
          <p class="mt-5 text-base leading-relaxed text-muted-foreground">
            Анкета — це бронювання місця й найкращої ціни, а не оплата. Ми
            зв'яжемося з вами особисто після закриття передзапису.
          </p>
          <div class="mt-8 rounded-xl border border-primary/40 bg-primary/10 p-5">
            <p class="text-sm font-bold text-primary">Дедлайн</p>
            <p class="mt-1 text-sm leading-relaxed text-foreground/90">
              Передзапис відкритий до <span class="font-extrabold">15.09</span>.
              Далі — старт продажів на загальних умовах.
            </p>
          </div>
        </div>

        <div
          v-if="sent"
          class="flex flex-col items-start justify-center rounded-2xl border border-primary/40 bg-primary/10 p-8"
        >
          <span class="text-4xl">✅</span>
          <h3 class="mt-4 font-display text-2xl font-bold">Заявку отримано!</h3>
          <p class="mt-2 text-sm leading-relaxed text-muted-foreground">
            Ми зв'яжемося з вами особисто, щойно відкриються продажі, і повідомимо
            найкращу ціну першими.
          </p>
        </div>
        <form v-else @submit.prevent="handleSubmit" class="flex flex-col gap-8">
          <label class="block">
            <span class="sr-only">Ім'я</span>
            <input
              required
              type="text"
              placeholder="Ім'я"
              class="w-full border-b border-input bg-transparent py-3 text-base outline-none placeholder:text-muted-foreground focus:border-primary"
            />
          </label>
          <label class="block">
            <span class="sr-only">Email</span>
            <input
              required
              type="email"
              placeholder="Email"
              class="w-full border-b border-input bg-transparent py-3 text-base outline-none placeholder:text-muted-foreground focus:border-primary"
            />
          </label>
          <fieldset>
            <legend class="text-sm text-muted-foreground">
              Ви вже проходили в нас «Основи інвестування» чи «Інвестування у
              фондовий ринок»?
            </legend>
            <div class="mt-3 flex flex-wrap gap-2.5">
              <button
                v-for="opt in priorOptions"
                :key="opt"
                type="button"
                @click="prior = opt"
                :class="[
                  'rounded-xl border px-5 py-2.5 text-sm font-semibold transition-colors',
                  prior === opt
                    ? 'border-primary bg-primary text-primary-foreground'
                    : 'border-input text-foreground hover:border-primary/60',
                ]"
              >
                {{ opt }}
              </button>
            </div>
          </fieldset>
          <button
            type="submit"
            class="group mt-2 inline-flex w-fit items-center gap-3 rounded-xl bg-primary px-7 py-4 text-base font-bold text-primary-foreground transition-transform hover:-translate-y-0.5"
          >
            Залишити заявку
            <span
              class="grid size-8 place-items-center rounded-lg bg-background text-primary transition-transform group-hover:translate-x-0.5"
            >
              ↘
            </span>
          </button>
        </form>
      </div>
    </section>

    <!-- FAQ -->
    <section class="mx-auto max-w-4xl px-5 pb-24 sm:px-8">
      <h2 class="font-display text-4xl font-extrabold leading-tight tracking-tight sm:text-5xl">
        Питання та <mark class="mark-accent">відповіді</mark>
      </h2>
      <div class="mt-10 divide-y divide-border border-y border-border">
        <details v-for="f in faqs" :key="f.q" class="group py-6">
          <summary class="flex cursor-pointer list-none items-start justify-between gap-4">
            <span class="text-lg font-bold">{{ f.q }}</span>
            <span class="mt-0.5 shrink-0 text-2xl font-light text-primary transition-transform group-open:rotate-45">
              +
            </span>
          </summary>
          <p class="mt-4 max-w-3xl text-base leading-relaxed text-muted-foreground">{{ f.a }}</p>
        </details>
      </div>
    </section>

    <!-- Final CTA -->
    <footer class="border-t border-border">
      <div
        class="mx-auto flex max-w-6xl flex-col items-start gap-8 px-5 py-16 sm:px-8 md:flex-row md:items-center md:justify-between"
      >
        <div>
          <h2 class="font-display text-3xl font-extrabold leading-tight tracking-tight sm:text-4xl">
            Готові перейти від знань до рішень?
          </h2>
          <p class="mt-3 text-muted-foreground">Передзапис відкритий до 15.09.</p>
        </div>
        <CtaButton class-name="shrink-0" />
      </div>
      <div class="mx-auto max-w-6xl border-t border-border px-5 py-6 sm:px-8">
        <p class="text-xs text-muted-foreground">
          школа останнього капіталіста · Просунуте інвестування · передзапис до 15.09
        </p>
      </div>
    </footer>
  </div>
</template>
