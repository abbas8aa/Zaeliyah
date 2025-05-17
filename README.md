# Zaeliyah
import { Card, CardContent } from "@/components/ui/card";
import { Button } from "@/components/ui/button";
import { Input } from "@/components/ui/input";
import { useState } from "react";
import Image from "next/image";

export default function Home() {
  return (
    <div className="bg-black text-white min-h-screen font-sans">
      {/* Header */}
      <header className="p-6 flex justify-between items-center border-b border-gray-700">
        <Image src="/IMG-20250516-WA0036.jpg" alt="Zaeliyah Logo" width={150} height={60} />
        <nav className="space-x-6">
          <a href="#home" className="hover:text-gold">Home</a>
          <a href="#collections" className="hover:text-gold">Collections</a>
          <a href="#about" className="hover:text-gold">About</a>
          <a href="#contact" className="hover:text-gold">Contact</a>
        </nav>
      </header>

      {/* Hero Section */}
      <section className="text-center py-24 bg-gradient-to-r from-black to-gray-900">
        <h1 className="text-5xl font-bold mb-4 text-gold">Elegance Woven to Perfection</h1>
        <p className="text-lg text-gray-300 max-w-xl mx-auto">
          Discover the luxurious world of Zaeliyah — where every thread whispers sophistication.
        </p>
        <Button className="mt-8 bg-gold text-black text-lg px-6 py-3 rounded-2xl shadow-lg">Shop Now</Button>
      </section>

      {/* Collections */}
      <section id="collections" className="py-16 px-8 bg-black">
        <h2 className="text-3xl text-gold font-semibold mb-8 text-center">Our Collections</h2>
        <div className="grid grid-cols-1 md:grid-cols-3 gap-6">
          {['Silk Series', 'Evening Elegance', 'Modern Royals'].map((collection) => (
            <Card key={collection} className="bg-gray-900 border-gold border">
              <CardContent className="p-6">
                <h3 className="text-xl font-semibold text-white mb-2">{collection}</h3>
                <p className="text-gray-400">Explore our {collection.toLowerCase()} range.</p>
              </CardContent>
            </Card>
          ))}
        </div>
      </section>

      {/* About */}
      <section id="about" className="py-16 px-8 bg-gradient-to-l from-black to-gray-800 text-center">
        <h2 className="text-3xl font-bold text-gold mb-6">About Zaeliyah</h2>
        <p className="max-w-2xl mx-auto text-gray-300">
          Zaeliyah is a celebration of craftsmanship and elegance. We create premium clothing for those who value grace, detail, and timeless fashion.
        </p>
      </section>

      {/* Contact */}
      <section id="contact" className="py-16 px-8 bg-black text-center">
        <h2 className="text-3xl font-bold text-gold mb-6">Get In Touch</h2>
        <form className="max-w-lg mx-auto space-y-4">
          <Input placeholder="Your Name" className="bg-gray-800 text-white" />
          <Input placeholder="Email Address" className="bg-gray-800 text-white" />
          <Input placeholder="Your Message" className="bg-gray-800 text-white" />
          <Button className="bg-gold text-black px-6 py-2 rounded-2xl">Send Message</Button>
        </form>
      </section>

      {/* Footer */}
      <footer className="py-6 text-center border-t border-gray-700">
        <p className="text-gray-500">© 2025 Zaeliyah. All rights reserved.</p>
      </footer>
    </div>
  );
}

const gold = {
  color: "#d4af37"
};
