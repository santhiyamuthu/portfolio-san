import React from "react";
import { motion } from "framer-motion";
import { FaLinkedin, FaEnvelope, FaPhone, FaExternalLinkAlt } from "react-icons/fa";

const projects = [
{
    title: "Wildeye",
    description: "Wildlife Surveillance & Alert System using Python and Flutter",
    link: "#"
  },
  {
    title: "Library Management System",
    description: "Python + MySQL with text-to-speech & data visualization",
    link: "#"
  },
  {
    title: "Smart e-Learning App",
    description: "Flutter & Firebase-based secure e-learning platform",
    link: "#"
  }
];

export default function Portfolio() {
  return (
    <div className="bg-gradient-to-r from-purple-600 via-pink-500 to-red-500 min-h-screen p-6 text-white font-sans">
      <header className="text-center mb-10">
        <motion.h1 
          className="text-4xl md:text-6xl font-bold mb-4"
          initial={{ opacity: 0, y: -50 }}
          animate={{ opacity: 1, y: 0 }}
        >
          Santhiya Muthu
        </motion.h1>
        <motion.p 
          className="text-lg md:text-xl"
          initial={{ opacity: 0 }}
          animate={{ opacity: 1 }}
          transition={{ delay: 0.5 }}
        >
          IT Student | Python, Flutter Developer | Creative Thinker
        </motion.p>
        <div className="flex justify-center gap-6 mt-4">
          <a href="mailto:santhiyamuthu914@gmail.com" target="_blank" rel="noreferrer" className="hover:scale-110 transition">
            <FaEnvelope size={28} />
          </a>
          <a href="https://www.linkedin.com/in/santhiya-muthu-275918221" target="_blank" rel="noreferrer" className="hover:scale-110 transition">
            <FaLinkedin size={28} />
          </a>
          <a href="tel:9487119928" className="hover:scale-110 transition">
            <FaPhone size={28} />
          </a>
        </div>
      </header>

      <section className="grid md:grid-cols-2 gap-8 mb-12">
        <motion.div className="bg-white bg-opacity-10 p-6 rounded-2xl shadow-xl" whileHover={{ scale: 1.05 }}>
          <h2 className="text-2xl font-semibold mb-2">Education</h2>
          <p>B.Tech IT, Sathyabama Institute (2021-2025) - CGPA: 7.71</p>
        </motion.div>
        <motion.div className="bg-white bg-opacity-10 p-6 rounded-2xl shadow-xl" whileHover={{ scale: 1.05 }}>
          <h2 className="text-2xl font-semibold mb-2">Skills</h2>
          <p>Python, Flutter, MySQL, HTML, Communication, Teamwork, Creativity</p>
        </motion.div>
      </section>

      <section className="mb-12">
        <h2 className="text-3xl font-bold mb-4 text-center">Project Gallery</h2>
        <div className="grid md:grid-cols-3 gap-6">
          {projects.map((proj, index) => (
            <motion.div 
              key={index} 
              className="bg-white bg-opacity-10 p-4 rounded-2xl shadow-lg"
              whileHover={{ scale: 1.05 }}
            >
              <h3 className="text-xl font-semibold mb-2">{proj.title}</h3>
              <p className="mb-2">{proj.description}</p>
              <a href={proj.link} target="_blank" rel="noreferrer" className="inline-flex items-center text-sm underline hover:text-yellow-200">
                View Project <FaExternalLinkAlt className="ml-1" />
              </a>
            </motion.div>
          ))}
        </div>
      </section>

      <footer className="text-center opacity-70 text-sm mt-8">
        © {new Date().getFullYear()} Santhiya Muthu. All rights reserved.
      </footer>
    </div>
  );
}
