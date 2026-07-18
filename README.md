import React from 'react';
import { motion } from 'framer-motion';
import { Github, Linkedin, Mail, Code, Terminal, Layers, ArrowUpRight } from 'lucide-react';

export default function Portfolio() {
  // Animation Variants for smooth, professional motion
  const fadeInUp = {
    hidden: { opacity: 0, y: 30 },
    visible: { opacity: 1, y: 0, transition: { duration: 0.6, ease: "easeOut" } }
  };

  const staggerContainer = {
    hidden: { opacity: 0 },
    visible: { opacity: 1, transition: { staggerChildren: 0.15 } }
  };

  return (
    <div className="min-h-screen bg-[#0B0F19] text-slate-100 font-sans selection:bg-cyan-500 selection:text-slate-900 overflow-x-hidden">
      
      {/* Background Ambient Glows */}
      <div className="absolute top-0 left-1/4 w-96 h-96 bg-blue-600/10 rounded-full blur-[120px] pointer-events-none" />
      <div className="absolute top-1/3 right-1/4 w-[400px] h-[400px] bg-cyan-600/5 rounded-full blur-[150px] pointer-events-none" />

      {/* Header / Navigation */}
      <nav className="sticky top-0 z-50 backdrop-blur-md bg-[#0B0F19]/70 border-b border-slate-800/50 px-6 py-4 transition-all duration-300">
        <div className="max-w-6xl mx-auto flex justify-between items-center">
          <motion.span 
            initial={{ opacity: 0, x: -20 }}
            animate={{ opacity: 1, x: 0 }}
            className="text-xl font-bold tracking-wider bg-gradient-to-r from-cyan-400 to-blue-500 bg-clip-text text-transparent"
          >
            PRADEEP P
          </motion.span>
          <div className="flex gap-6 text-sm text-slate-400 font-medium">
            <a href="#about" className="hover:text-cyan-400 transition-colors duration-200">About</a>
            <a href="#skills" className="hover:text-cyan-400 transition-colors duration-200">Skills</a>
            <a href="#projects" className="hover:text-cyan-400 transition-colors duration-200">Project</a>
          </div>
        </div>
      </nav>

      {/* Hero Section */}
      <section id="about" className="max-w-6xl mx-auto px-6 pt-24 pb-20 flex flex-col justify-center min-h-[80vh] relative z-10">
        <motion.div 
          initial="hidden"
          animate="visible"
          variants={staggerContainer}
          className="space-y-6 max-w-3xl"
        >
          <motion.p variants={fadeInUp} className="text-cyan-400 font-mono tracking-widest text-sm uppercase">
            // Software Engineer Portfolio
          </motion.p>
          
          <motion.h1 variants={fadeInUp} className="text-5xl md:text-7xl font-extrabold tracking-tight text-white">
            Hi, I'm <span className="bg-gradient-to-r from-white via-slate-200 to-slate-400 bg-clip-text text-transparent">Pradeep P.</span>
          </motion.h1>

          <motion.h2 variants={fadeInUp} className="text-3xl md:text-4xl font-bold text-slate-400">
            Specializing in robust backend systems and core algorithms.
          </motion.h2>

          <motion.p variants={fadeInUp} className="text-lg text-slate-400 leading-relaxed max-w-2xl">
            Focused on building high-performance applications through clean object-oriented architecture and optimal data structures. Passionate about decentralized architectures and secure system design.
          </motion.p>

          {/* Social Links & Call to Action */}
          <motion.div variants={fadeInUp} className="flex flex-wrap gap-4 pt-4">
            <a 
              href="mailto:pradeepxz18@gmail.com" 
              className="flex items-center gap-2 bg-gradient-to-r from-cyan-500 to-blue-600 hover:from-cyan-400 hover:to-blue-500 text-slate-950 font-semibold px-6 py-3 rounded-lg shadow-lg shadow-cyan-500/10 hover:shadow-cyan-500/20 hover:-translate-y-0.5 transition-all duration-200"
            >
              <Mail size={18} /> Contact Me
            </a>
            
            <div className="flex gap-2">
              <a 
                href="https://github.com/pradeepdcruze" target="_blank" rel="noreferrer"
                className="p-3 bg-slate-900 hover:bg-slate-800 border border-slate-800 hover:border-slate-700 text-slate-300 hover:text-cyan-400 rounded-lg transition-all duration-200"
                aria-label="GitHub"
              >
                <Github size={20} />
              </a>
              <a 
                href="https://www.linkedin.com/in/pradeep-p-316711336" target="_blank" rel="noreferrer"
                className="p-3 bg-slate-900 hover:bg-slate-800 border border-slate-800 hover:border-slate-700 text-slate-300 hover:text-cyan-400 rounded-lg transition-all duration-200"
                aria-label="LinkedIn"
              >
                <Linkedin size={20} />
              </a>
            </div>
          </motion.div>
        </motion.div>
      </section>

      {/* Technical Focus / Skills Section */}
      <section id="skills" className="max-w-6xl mx-auto px-6 py-20 border-t border-slate-900">
        <motion.div 
          initial="hidden"
          whileInView="visible"
          viewport={{ once: true, margin: "-100px" }}
          variants={staggerContainer}
          className="space-y-12"
        >
          <motion.div variants={fadeInUp} className="space-y-2">
            <h2 className="text-3xl font-bold tracking-tight text-white">Technical Core</h2>
            <div className="h-1 w-12 bg-cyan-500 rounded" />
          </motion.div>

          <div className="grid md:grid-cols-2 gap-6">
            {/* Java Card */}
            <motion.div 
              variants={fadeInUp}
              whileHover={{ y: -5, borderColor: "rgba(34, 211, 238, 0.3)" }}
              className="p-8 bg-[#0F1524] border border-slate-800/80 rounded-xl transition-all duration-300 group shadow-xl"
            >
              <div className="p-3 bg-cyan-500/10 text-cyan-400 rounded-lg w-fit mb-6 group-hover:bg-cyan-500 group-hover:text-slate-950 transition-colors duration-300">
                <Code size={24} />
              </div>
              <h3 className="text-xl font-bold text-white mb-3">Java Development</h3>
              <p className="text-slate-400 leading-relaxed">
                Proficient in building scalable enterprise logic, object-oriented software engineering, and clean, modular architecture.
              </p>
            </motion.div>

            {/* DSA Card */}
            <motion.div 
              variants={fadeInUp}
              whileHover={{ y: -5, borderColor: "rgba(59, 130, 246, 0.3)" }}
              className="p-8 bg-[#0F1524] border border-slate-800/80 rounded-xl transition-all duration-300 group shadow-xl"
            >
              <div className="p-3 bg-blue-500/10 text-blue-400 rounded-lg w-fit mb-6 group-hover:bg-blue-500 group-hover:text-slate-950 transition-colors duration-300">
                <Terminal size={24} />
              </div>
              <h3 className="text-xl font-bold text-white mb-3">Data Structures & Algorithms</h3>
              <p className="text-slate-400 leading-relaxed">
                Strong foundation in analytical problem-solving, optimization strategies, complexity analysis, and efficient code execution.
              </p>
            </motion.div>
          </div>
        </motion.div>
      </section>

      {/* Featured Projects Section */}
      <section id="projects" className="max-w-6xl mx-auto px-6 py-20 border-t border-slate-900 mb-20">
        <motion.div 
          initial="hidden"
          whileInView="visible"
          viewport={{ once: true, margin: "-100px" }}
          variants={staggerContainer}
          className="space-y-12"
        >
          <motion.div variants={fadeInUp} className="space-y-2">
            <h2 className="text-3xl font-bold tracking-tight text-white">Academic Focus</h2>
            <div className="h-1 w-12 bg-blue-500 rounded" />
          </motion.div>

          {/* Single Featured Project Showcase */}
          <motion.div 
            variants={fadeInUp}
            whileHover={{ y: -4 }}
            className="relative bg-gradient-to-b from-[#0F1524] to-[#0D1220] border border-slate-800/80 rounded-2xl p-8 md:p-12 shadow-2xl overflow-hidden group transition-all duration-300"
          >
            <div className="absolute top-0 right-0 w-64 h-64 bg-cyan-500/5 rounded-full blur-3xl pointer-events-none group-hover:bg-cyan-500/10 transition-colors duration-500" />
            
            <div className="max-w-2xl space-y-6">
              <div className="flex items-center gap-2 text-cyan-400 font-mono text-sm">
                <Layers size={16} /> Featured Architecture Project
              </div>
              
              <h3 className="text-2xl md:text-3xl font-bold text-white group-hover:text-cyan-400 transition-colors duration-200">
                Secure & Decentralized Identity Verification System
              </h3>
              
              <p className="text-slate-400 leading-relaxed text-base md:text-lg">
                An advanced cryptographic identity architecture engineered to eliminate centralized single points of failure. Provides absolute data privacy, self-sovereign user management, and seamless, tamper-proof security validation protocols.
              </p>

              <div className="flex flex-wrap gap-2 pt-2">
                {['Java', 'Decentralized Architecture', 'Cryptographic Security', 'Data Structures'].map((tech) => (
                  <span key={tech} className="text-xs font-mono bg-slate-900 text-slate-300 border border-slate-800 px-3 py-1.5 rounded-md">
                    {tech}
                  </span>
                ))}
              </div>

              <div className="pt-4 flex gap-4">
                <a 
                  href="https://github.com/pradeepdcruze" target="_blank" rel="noreferrer"
                  className="inline-flex items-center gap-2 text-sm font-semibold text-white hover:text-cyan-400 transition-colors duration-200"
                >
                  View Repository <ArrowUpRight size={16} />
                </a>
              </div>
            </div>
          </motion.div>
        </motion.div>
      </section>

      {/* Footer */}
      <footer className="border-t border-slate-900/60 bg-[#070A12] py-8 text-center text-xs text-slate-500 font-mono">
        <p>© 2026 PRADEEP P. All rights reserved.</p>
      </footer>
    </div>
  );
}