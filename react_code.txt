import React from "react";
import { BrowserRouter as Router, Route, Routes, Link } from "react-router-dom";
import { Card, CardContent } from "@/components/ui/card";
import { Button } from "@/components/ui/button";

const Home = () => (
  <div className="p-6 text-center">
    <h1 className="text-4xl font-bold">Welcome to SaasTechConsultancy</h1>
    <p className="text-lg mt-4">Empowering businesses with SaaS, AI, and ML solutions.</p>
    <Button className="mt-4" asChild>
      <Link to="/services">Explore Our Services</Link>
    </Button>
  </div>
);

const About = () => (
  <div className="p-6">
    <h2 className="text-3xl font-bold">About Us</h2>
    <p className="mt-4 text-lg">
      SaasTechConsultancy was founded to revolutionize the tech industry by providing cutting-edge SaaS,
      AI, and ML solutions. Our goal is to help businesses scale efficiently with innovative technology.
    </p>
  </div>
);

const Services = () => (
  <div className="p-6">
    <h2 className="text-3xl font-bold">Our Services</h2>
    <div className="grid grid-cols-1 md:grid-cols-3 gap-6 mt-6">
      <Card>
        <CardContent>
          <h3 className="text-xl font-bold">SaaS Solutions</h3>
          <p className="mt-2">Custom-built software solutions to automate business processes.</p>
        </CardContent>
      </Card>
      <Card>
        <CardContent>
          <h3 className="text-xl font-bold">AI & ML Consulting</h3>
          <p className="mt-2">Leveraging AI and ML to optimize and innovate your business.</p>
        </CardContent>
      </Card>
      <Card>
        <CardContent>
          <h3 className="text-xl font-bold">Offshore IT Services</h3>
          <p className="mt-2">Providing skilled offshore talent for development and support.</p>
        </CardContent>
      </Card>
    </div>
  </div>
);

const Contact = () => (
  <div className="p-6">
    <h2 className="text-3xl font-bold">Contact Us</h2>
    <p className="mt-4">Email: contact@saastechconsultancy.com</p>
    <p>Phone: +1-123-456-7890</p>
  </div>
);

const App = () => (
  <Router>
    <div className="min-h-screen bg-gray-100 text-gray-900">
      <nav className="bg-blue-500 text-white p-4 flex justify-between">
        <Link to="/" className="font-bold text-lg">SaasTechConsultancy</Link>
        <div>
          <Link to="/about" className="mr-4">About</Link>
          <Link to="/services" className="mr-4">Services</Link>
          <Link to="/contact">Contact</Link>
        </div>
      </nav>
      <Routes>
        <Route path="/" element={<Home />} />
        <Route path="/about" element={<About />} />
        <Route path="/services" element={<Services />} />
        <Route path="/contact" element={<Contact />} />
      </Routes>
    </div>
  </Router>
);

export default App;
