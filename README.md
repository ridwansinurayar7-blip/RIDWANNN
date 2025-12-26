import { motion } from "framer-motion";
import { Button } from "@/components/ui/button";
import { Card, CardContent } from "@/components/ui/card";
import { Sparkles, Cpu, Globe, Shield } from "lucide-react";

export default function AdvancedWebsite() {
  return (
    <div className="min-h-screen bg-gradient-to-br from-black via-slate-900 to-indigo-950 text-white">
      {/* Hero Section */}
      <section className="flex flex-col items-center justify-center text-center px-6 py-32">
        <motion.h1
          initial={{ opacity: 0, y: 20 }}
          animate={{ opacity: 1, y: 0 }}
          transition={{ duration: 0.8 }}
          className="text-5xl md:text-7xl font-bold mb-6"
        >
          Website Canggih
        </motion.h1>
        <p className="max-w-2xl text-lg md:text-xl text-slate-300 mb-8">
          Platform modern dengan teknologi AI, desain futuristik, dan performa kelas dunia.
        </p>
        <Button size="lg" className="rounded-2xl px-8 py-6 text-lg">
          Mulai Sekarang
        </Button>
      </section>

      {/* Features */}
      <section className="grid grid-cols-1 md:grid-cols-4 gap-6 px-8 pb-32">
        {[{ icon: Sparkles, title: "AI Ready", desc: "Siap integrasi kecerdasan buatan." },
          { icon: Cpu, title: "Fast", desc: "Performa sangat cepat & ringan." },
          { icon: Globe, title: "Global", desc: "Siap digunakan seluruh dunia." },
          { icon: Shield, title: "Secure", desc: "Keamanan tingkat tinggi." }]
          .map((f, i) => (
            <motion.div
              key={i}
              whileHover={{ scale: 1.05 }}
              className="h-full"
            >
              <Card className="bg-white/5 border-white/10 rounded-2xl h-full">
                <CardContent className="p-6 text-center">
                  <f.icon className="mx-auto mb-4 h-10 w-10 text-indigo-400" />
                  <h3 className="text-xl font-semibold mb-2">{f.title}</h3>
                  <p className="text-slate-400 text-sm">{f.desc}</p>
                </CardContent>
              </Card>
            </motion.div>
          ))}
      </section>

      {/* Footer */}
      <footer className="text-center text-slate-500 pb-10">
        © 2025 Website Canggih by Lyra
      </footer>
    </div>
  );
}
