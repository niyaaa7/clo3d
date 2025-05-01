# clo3d
import React from "react";
import { Button } from "@/components/ui/button";
import { Card, CardContent } from "@/components/ui/card";
import { PlayCircle } from "lucide-react";

export default function CLO3DStyleSite() {
  return (
    <div className="min-h-screen bg-gray-950 text-white font-sans">
      {/* Header */}
      <header className="flex justify-between items-center px-8 py-6 bg-gray-900 shadow-md">
        <h1 className="text-2xl font-bold">CLO3D Inspired</h1>
        <nav className="space-x-6">
          <a href="#features" className="hover:text-blue-400">Recursos</a>
          <a href="#plans" className="hover:text-blue-400">Planos</a>
          <a href="#download" className="hover:text-blue-400">Download</a>
        </nav>
      </header>

      {/* Hero Section */}
      <section className="flex flex-col items-center justify-center text-center px-6 py-24 bg-gradient-to-br from-gray-800 to-black">
        <h2 className="text-4xl md:text-6xl font-extrabold mb-6">Design 3D de Moda, Reimaginado</h2>
        <p className="text-lg md:text-xl text-gray-300 max-w-2xl mb-8">
          Visualize roupas em tempo real com precisão física e estilística usando ferramentas de última geração.
        </p>
        <Button size="lg" className="text-lg">Experimente Agora</Button>
      </section>

      {/* Video Preview */}
      <section className="px-4 py-20 bg-gray-900 flex justify-center">
        <Card className="w-full max-w-4xl overflow-hidden">
          <CardContent className="p-0">
            <div className="relative">
              <video
                className="w-full h-auto"
                controls
                poster="https://dummyimage.com/1280x720/000/fff.jpg&text=Preview"
              >
                <source src="/video.mp4" type="video/mp4" />
                Seu navegador não suporta vídeo HTML5.
              </video>
              <div className="absolute inset-0 flex items-center justify-center">
                <PlayCircle className="w-20 h-20 text-white/80" />
              </div>
            </div>
          </CardContent>
        </Card>
      </section>

      {/* Footer */}
      <footer className="text-center text-gray-500 text-sm py-6 bg-gray-950 border-t border-gray-800">
        © {new Date().getFullYear()} CLO3D Inspired. Todos os direitos reservados.
      </footer>
    </div>
  );
}
