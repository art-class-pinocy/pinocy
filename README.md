import React from "react";
import { motion } from "framer-motion";
import { Button } from "@/components/ui/button";
import { Card, CardContent, CardHeader, CardTitle } from "@/components/ui/card";
import { Badge } from "@/components/ui/badge";
import { Paintbrush, Calendar, MapPin, Leaf, Clock, Users } from "lucide-react";

export default function ArtClassPinocy() {
  const features = [
    {
      icon: <Paintbrush className="h-6 w-6" aria-hidden />,
      title: "多彩なプログラム",
      desc: "アクリル画・水彩画・デッサン・クロッキーなど。楽しく作りながら上達します。",
    },
    {
      icon: <Users className="h-6 w-6" aria-hidden />,
      title: "対象: 年少〜大人",
      desc: "幅広い年齢に合わせて、安心して学べるカリキュラムを用意。",
    },
    {
      icon: <Calendar className="h-6 w-6" aria-hidden />,
      title: "月2回・予約制",
      desc: "お好きな日時を選べます。毎週土曜日は定期クラスも開催。",
    },
    {
      icon: <Leaf className="h-6 w-6" aria-hidden />,
      title: "道具は教室で用意",
      desc: "手ぶらでOK。汚れてもよい服装でお越しください。",
    },
  ];

  const schedule = [
    { time: "10:00–11:30", note: "毎週土曜日" },
    { time: "14:00–15:30", note: "毎週土曜日" },
  ];

  const pricing = [
    { name: "体験(1回)", price: "¥2,000", details: "まずは雰囲気をお試し" },
    { name: "月2回", price: "¥4,000", details: "継続して通いたい方に" },
  ];

  return (
    <div className="min-h-screen bg-amber-50 text-stone-900">
      {/* Header */}
      <header className="sticky top-0 z-40 backdrop-blur bg-amber-50/80 border-b">
        <div className="mx-auto max-w-6xl px-4 sm:px-6 flex items-center justify-between h-16">
          <div className="flex items-center gap-3">
            <div className="h-10 w-10 grid place-items-center rounded-full bg-lime-200 border">
              <Leaf className="h-6 w-6" aria-hidden />
            </div>
            <div>
              <p className="text-xs uppercase tracking-widest text-stone-500">Art class</p>
              <p className="text-2xl font-black tracking-tight">Pinocy</p>
            </div>
          </div>
          <nav className="hidden md:flex items-center gap-6 text-sm">
            <a href="#about" className="hover:opacity-80">教室について</a>
            <a href="#classes" className="hover:opacity-80">クラス&料金</a>
            <a href="#schedule" className="hover:opacity-80">スケジュール</a>
            <a href="#access" className="hover:opacity-80">アクセス</a>
          </nav>
          <Button asChild className="rounded-2xl">
            <a href="#contact">LINEで予約</a>
          </Button>
        </div>
      </header>

      {/* Hero */}
      <section className="relative overflow-hidden">
        <div className="absolute inset-0 bg-[radial-gradient(60rem_60rem_at_10%_-10%,#fde68a_0%,transparent_50%),radial-gradient(60rem_60rem_at_110%_10%,#bbf7d0_0%,transparent_50%)]" />
        <div className="relative mx-auto max-w-6xl px-4 sm:px-6 py-16 md:py-24 grid md:grid-cols-2 gap-10 items-center">
          <div>
            <motion.h1
              initial={{ opacity: 0, y: 20 }}
              animate={{ opacity: 1, y: 0 }}
              transition={{ duration: 0.6 }}
              className="text-4xl md:text-5xl font-black leading-tight tracking-tight"
            >
              2025年9月 START
            </motion.h1>
            <p className="mt-4 text-lg leading-relaxed">
              幼稚園や学校の図工では体験できない、もっと深い「アートの世界」へ。自由な発想で、楽しく表現しながら技法を学ぶアート教室です。
            </p>
            <div className="mt-6 flex flex-wrap items-center gap-3">
              <Badge variant="secondary" className="rounded-full">年少さん〜大人まで</Badge>
              <Badge variant="secondary" className="rounded-full">道具は教室で用意</Badge>
              <Badge variant="secondary" className="rounded-full">月2回・予約制</Badge>
            </div>
            <div className="mt-8 flex gap-3">
              <Button asChild size="lg" className="rounded-2xl">
                <a href="#contact">体験レッスンを予約</a>
              </Button>
              <Button asChild variant="outline" size="lg" className="rounded-2xl">
                <a href="#classes">カリキュラムを見る</a>
              </Button>
            </div>
          </div>
          <div className="relative">
            <div className="aspect-[4/3] w-full rounded-3xl overflow-hidden ring-1 ring-black/5 shadow-xl bg-white">
              <img
                src="https://images.unsplash.com/photo-1513364776144-60967b0f800f?q=80&w=1600&auto=format&fit=crop"
                alt="Pinocyの作品例"
                className="h-full w-full object-cover"
                loading="lazy"
              />
            </div>
            <div className="absolute -bottom-4 -left-4 hidden md:block">
              <Card className="rounded-2xl shadow-lg">
                <CardContent className="p-3 flex items-center gap-2">
                  <Clock className="h-4 w-4" />
                  <span className="text-sm">レッスン90分</span>
                </CardContent>
              </Card>
            </div>
          </div>
        </div>
      </section>

      {/* About */}
      <section id="about" className="mx-auto max-w-6xl px-4 sm:px-6 py-16">
        <div className="grid md:grid-cols-2 gap-10 items-start">
          <div>
            <h2 className="text-3xl md:text-4xl font-extrabold tracking-tight">Pinocyについて</h2>
            <p className="mt-4 leading-relaxed">
              新しい感性や技術を楽しく学びながら、作る喜びを味わえる少人数制の教室です。色々な技法を体験しながら、アートの広がりを楽しみます。
              「ただ作る」だけではなく、作品を通して自分の感性に気づいたり、新しい表現方法を一緒に発見していきましょう。
            </p>
            <ul className="mt-6 space-y-3">
              {features.map((f, i) => (
                <li key={i} className="flex items-start gap-3">
                  <div className="mt-1 text-stone-700">{f.icon}</div>
                  <div>
                    <p className="font-semibold">{f.title}</p>
                    <p className="text-sm text-stone-600">{f.desc}</p>
                  </div>
                </li>
              ))}
            </ul>
          </div>
          <div>
            <Card className="rounded-3xl">
              <CardHeader>
                <CardTitle>講師プロフィール</CardTitle>
              </CardHeader>
              <CardContent className="space-y-4">
                <p>
                  講師: 千尋（イラストレーター） / 美大卒・美術科教員免許あり。
                </p>
                <p className="text-sm text-stone-600">
                  子どもから大人まで、一人ひとりのペースに合わせて丁寧にサポートします。
                </p>
              </CardContent>
            </Card>
          </div>
        </div>
      </section>

      {/* Classes & Pricing */}
      <section id="classes" className="mx-auto max-w-6xl px-4 sm:px-6 py-16 bg-white/60 rounded-3xl">
        <h2 className="text-3xl md:text-4xl font-extrabold tracking-tight">クラス & 料金</h2>
        <p className="mt-3 text-stone-700">カリキュラム例: アクリル画 / 水彩画 / デッサン / クロッキー など</p>
        <div className="mt-8 grid sm:grid-cols-2 gap-6">
          {pricing.map((p) => (
            <Card key={p.name} className="rounded-3xl">
              <CardHeader>
                <CardTitle className="flex items-center justify-between">
                  <span>{p.name}</span>
                  <span className="text-2xl font-black">{p.price}</span>
                </CardTitle>
              </CardHeader>
              <CardContent>
                <p className="text-sm text-stone-600">{p.details}</p>
              </CardContent>
            </Card>
          ))}
        </div>
        <div className="mt-6">
          <Button asChild size="lg" className="rounded-2xl">
            <a href="#contact">体験レッスンを申し込む</a>
          </Button>
        </div>
      </section>

      {/* Schedule */}
      <section id="schedule" className="mx-auto max-w-6xl px-4 sm:px-6 py-16">
        <h2 className="text-3xl md:text-4xl font-extrabold tracking-tight">スケジュール</h2>
        <p className="mt-3 text-stone-700">毎週土曜日（各90分）/ 予約制</p>
        <div className="mt-6 grid md:grid-cols-2 gap-6">
          {schedule.map((s, idx) => (
            <Card key={idx} className="rounded-3xl">
              <CardContent className="p-6 flex items-center gap-4">
                <Calendar className="h-6 w-6" />
                <div>
                  <p className="font-semibold">{s.time}</p>
                  <p className="text-sm text-stone-600">{s.note}</p>
                </div>
              </CardContent>
            </Card>
          ))}
        </div>
      </section>

      {/* Access */}
      <section id="access" className="mx-auto max-w-6xl px-4 sm:px-6 py-16">
        <h2 className="text-3xl md:text-4xl font-extrabold tracking-tight">アクセス</h2>
        <div className="mt-4 grid md:grid-cols-2 gap-6 items-start">
          <div className="space-y-2 text-stone-700">
            <p className="flex items-center gap-2"><MapPin className="h-5 w-5" /> 箕面市桜ヶ丘3丁目（詳細はご予約後にご案内）</p>
            <p>最寄: バス停・桜ヶ丘付近</p>
            <p>お車・自転車OK</p>
          </div>
          <div className="rounded-3xl overflow-hidden ring-1 ring-black/5 shadow">
            <iframe
              title="map"
              src="https://www.google.com/maps?q=%E7%AE%95%E9%9D%A2%E5%B8%82%E6%A1%9C%E3%83%B6%E4%B8%983%E4%B8%81%E7%9B%AE&output=embed"
              className="w-full h-80"
              loading="lazy"
              referrerPolicy="no-referrer-when-downgrade"
              allowFullScreen
            />
          </div>
        </div>
      </section>

      {/* Contact */}
      <section id="contact" className="mx-auto max-w-6xl px-4 sm:px-6 py-16">
        <Card className="rounded-3xl">
          <CardContent className="p-6 md:p-10 grid md:grid-cols-2 gap-8 items-center">
            <div>
              <h3 className="text-2xl md:text-3xl font-extrabold tracking-tight">体験・ご予約 / お問い合わせ</h3>
              <p className="mt-3 text-stone-700">
                ご相談だけでもお気軽にどうぞ。LINEで「体験希望」とメッセージいただくか、フォームからお申し込みください。
              </p>
              <div className="mt-6 flex flex-wrap gap-3">
                <Button asChild size="lg" className="rounded-2xl">
                  <a href="https://lin.ee/EY3yPyF" target="_blank" rel="noopener noreferrer" aria-label="LINEで予約">LINEで予約</a>
                </Button>
                <Button asChild variant="outline" size="lg" className="rounded-2xl">
                  <a href="https://docs.google.com/forms/d/11oXh90VbK_Le9vgHYLzMpsqiHk8AlH6NtPxOAqGC2Hg/edit#responses" target="_blank" rel="noopener noreferrer" aria-label="フォームで申し込み">フォームで申し込み</a>
                </Button>
              </div>
              <p className="mt-2 text-xs text-stone-500">※ 埋め込みが表示されない場合は「フォームで申し込み」から別タブで開いてください。</p>
            </div>
            <div className="aspect-square w-full rounded-3xl overflow-hidden bg-white ring-1 ring-black/5 grid place-items-center p-6">
              <img
                src="https://images.unsplash.com/photo-1513364776144-60967b0f800f?q=80&w=800&auto=format&fit=crop"
                alt="作品サンプル"
                className="h-full w-full object-cover rounded-2xl"
                loading="lazy"
              />
            </div>
          </CardContent>
        </Card>

        {/* Embedded form */}
        <Card className="rounded-3xl mt-8">
          <CardHeader>
            <CardTitle>体験レッスンお申し込みフォーム</CardTitle>
          </CardHeader>
          <CardContent>
            <div className="w-full h-[1000px] rounded-2xl overflow-hidden ring-1 ring-black/5">
              <iframe
                title="trial-form"
                src="https://docs.google.com/forms/d/11oXh90VbK_Le9vgHYLzMpsqiHk8AlH6NtPxOAqGC2Hg/edit#responses"
                className="w-full h-full"
                loading="lazy"
              />
            </div>
            <p className="mt-3 text-xs text-stone-500">Googleフォームの公開設定が必要です。編集用URLのままでは表示できない場合があります。公開用の「/viewform」URLに差し替えると安定します。</p>
          </CardContent>
        </Card>
      </section>

      {/* Footer */}
      <footer className="border-t py-10 text-sm">
        <div className="mx-auto max-w-6xl px-4 sm:px-6 flex flex-col md:flex-row items-center justify-between gap-4">
          <p className="text-stone-500">© {new Date().getFullYear()} Art class Pinocy</p>
          <div className="flex items-center gap-4">
            <a href="#about" className="hover:opacity-80">教室について</a>
            <a href="#classes" className="hover:opacity-80">料金</a>
            <a href="#contact" className="hover:opacity-80">お問い合わせ</a>
          </div>
        </div>
      </footer>
    </div>
  );
}

</html>
