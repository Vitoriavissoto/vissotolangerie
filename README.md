import React from "react";
import { Button } from "@/components/ui/button";
import { Card, CardContent } from "@/components/ui/card";
import { Input } from "@/components/ui/input";
import { motion } from "framer-motion";
import { MailIcon, TruckIcon, StarIcon } from "lucide-react";

export default function Home() {
  return (
    <div className="min-h-screen bg-gradient-to-b from-rose-100 to-purple-200 p-4 relative">
      {/* Botão fixo do WhatsApp */}
      <a
        href="https://wa.me/5515996628834"
        target="_blank"
        rel="noopener noreferrer"
        className="fixed bottom-6 right-6 bg-green-500 text-white px-4 py-3 rounded-full shadow-lg hover:bg-green-600 transition z-50"
      >
        WhatsApp
      </a>

      {/* Header */}
      <header className="flex justify-between items-center py-6 px-4 md:px-12">
        <h1 className="text-3xl font-bold text-rose-800">Vissoto Langerie</h1>
        <nav className="space-x-6 text-rose-700">
          <a href="#" className="hover:underline">Home</a>
          <a href="#categorias" className="hover:underline">Categorias</a>
          <a href="#produtos" className="hover:underline">Produtos</a>
          <a href="#contato" className="hover:underline">Contato</a>
        </nav>
      </header>

      {/* Banner */}
      <section className="w-full h-[500px] bg-cover bg-center rounded-3xl shadow-lg mb-12" style={{ backgroundImage: "url('/mnt/data/Imagem do WhatsApp de 2025-04-08 à(s) 19.19.38_802b17e0.jpg')" }}>
        <div className="w-full h-full bg-rose-900/30 rounded-3xl flex items-center justify-center">
          <h2 className="text-white text-5xl md:text-6xl font-bold text-center drop-shadow-xl">Sinta-se linda todos os dias</h2>
        </div>
      </section>

      {/* Sobre a marca */}
      <section className="text-center mb-12 max-w-3xl mx-auto">
        <h3 className="text-2xl font-bold text-rose-800 mb-4">Sobre a Vissoto Langerie</h3>
        <p className="text-rose-700 text-lg">Vissoto Langerie nasceu com o propósito de empoderar mulheres através de peças íntimas sofisticadas, confortáveis e irresistivelmente lindas. Cada detalhe é pensado para valorizar quem você é.</p>
      </section>

      {/* Categorias */}
      <section id="categorias" className="mb-12">
        <h3 className="text-2xl font-semibold text-rose-800 mb-6 text-center">Categorias</h3>
        <div className="grid grid-cols-2 md:grid-cols-5 gap-4 text-center">
          {['Calcinhas', 'Sutiãs', 'Conjuntos', 'Pijamas', 'Camisolas'].map(cat => (
            <div key={cat} className="bg-white rounded-xl shadow p-4 text-rose-800 font-medium hover:scale-105 transition">
              {cat}
            </div>
          ))}
        </div>
      </section>

      {/* Produtos em destaque */}
      <section id="produtos" className="py-8">
        <h3 className="text-2xl font-semibold text-rose-800 mb-6 text-center">Destaques</h3>
        <div className="grid grid-cols-1 md:grid-cols-3 gap-6">
          {[{
            src: "/mnt/data/Imagem do WhatsApp de 2025-04-08 à(s) 19.23.14_727f9d56.jpg",
            alt: "Conjunto Elegance"
          }, {
            src: "/mnt/data/Imagem do WhatsApp de 2025-04-08 à(s) 19.20.03_5acfa9ba.jpg",
            alt: "Conjunto Sensual Rosa"
          }, {
            src: "/mnt/data/Imagem do WhatsApp de 2025-04-08 à(s) 19.23.21_71d7c4d0.jpg",
            alt: "Camisola de Cetim"
          }].map((item, i) => (
            <motion.div
              key={i}
              whileHover={{ scale: 1.03 }}
              className="rounded-2xl shadow-md"
            >
              <Card className="rounded-2xl">
                <CardContent className="p-4">
                  <img src={item.src} alt={item.alt} className="rounded-xl mb-3" />
                  <p className="text-lg text-rose-900 font-medium">{item.alt}</p>
                </CardContent>
              </Card>
            </motion.div>
          ))}
        </div>
      </section>

      {/* Depoimentos */}
      <section className="py-12 text-center bg-white/70 rounded-3xl my-8">
        <h3 className="text-2xl font-semibold text-rose-800 mb-6">O que dizem nossas clientes</h3>
        <div className="space-y-4 max-w-3xl mx-auto text-rose-700">
          <p>"As peças são maravilhosas, confortáveis e me sinto poderosa com cada uma delas!" – <strong>Juliana R.</strong></p>
          <p>"Recebi super rápido! Atendimento impecável e produto de altíssima qualidade." – <strong>Renata M.</strong></p>
        </div>
      </section>

      {/* Como comprar */}
      <section className="text-center mb-12">
        <h3 className="text-2xl font-semibold text-rose-800 mb-6">Como comprar</h3>
        <ol className="list-decimal text-left max-w-xl mx-auto text-rose-700 space-y-2">
          <li>Escolha a peça que mais combina com você.</li>
          <li>Entre em contato pelo WhatsApp para finalizar sua compra.</li>
          <li>Receba no conforto da sua casa, em qualquer lugar do Brasil!</li>
        </ol>
      </section>

      {/* Newsletter */}
      <section className="text-center py-10 bg-rose-200/40 rounded-3xl mb-12">
        <h3 className="text-xl font-semibold text-rose-800 mb-2">Receba novidades e promoções</h3>
        <form className="flex justify-center gap-2 max-w-md mx-auto">
          <Input type="email" placeholder="Digite seu e-mail" className="rounded-full" />
          <Button className="bg-rose-700 text-white rounded-full hover:bg-rose-800">Enviar</Button>
        </form>
      </section>

      {/* Contato */}
      <section id="contato" className="py-12 text-center">
        <h3 className="text-2xl font-semibold text-rose-800 mb-4">Fale com a gente</h3>
        <p className="text-rose-700 mb-6">Estamos aqui para te ajudar com qualquer dúvida.</p>
        <a
          href="https://wa.me/5515996628834"
          target="_blank"
          rel="noopener noreferrer"
          className="inline-block bg-rose-700 text-white px-6 py-3 rounded-full shadow-md hover:bg-rose-800 transition"
        >
          Chamar no WhatsApp
        </a>
      </section>

      {/* Rodapé */}
      <footer className="mt-16 py-6 border-t border-rose-300 text-center text-rose-700">
        <div className="flex flex-col items-center gap-2">
          <p className="flex items-center gap-1"><TruckIcon size={16} /> Enviamos para todo o Brasil</p>
          <p className="flex items-center gap-1"><MailIcon size={16} /> contato@vissotolangerie.com</p>
          <p className="text-sm mt-2">Com amor, Vissoto Langerie © 2025</p>
        </div>
      </footer>
    </div>
  );
}
