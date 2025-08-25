# Green-Basket
Organic vegetables at your door step
import { useState } from "react"; import { Card, CardContent } from "@/components/ui/card"; import { Button } from "@/components/ui/button"; import { Input } from "@/components/ui/input";

export default function GreenBasket() { const [name, setName] = useState(""); const [phone, setPhone] = useState(""); const [plot, setPlot] = useState("Medium Plot");

const handleSubmit = () => { const message = Hello, I am ${name}, interested in ${plot}. My phone is ${phone}.; window.open(https://wa.me/91XXXXXXXXXX?text=${encodeURIComponent(message)}); };

return ( <div className="min-h-screen bg-green-50 text-gray-800"> {/* Hero Section */} <div className="bg-green-600 text-white text-center py-12"> <h1 className="text-4xl font-bold mb-4">Green Basket</h1> <p className="text-lg">Your Own Organic Farm – Without the Work!</p> </div>

{/* Pricing Plans */}
  <div className="max-w-5xl mx-auto py-12 px-4 grid md:grid-cols-3 gap-6">
    <Card className="shadow-lg">
      <CardContent className="p-6 text-center">
        <h2 className="text-xl font-bold mb-2">Small Plot</h2>
        <p className="mb-2">10 sq ft</p>
        <p className="text-green-600 font-bold mb-4">₹1,200 / 3 months</p>
        <Button onClick={() => setPlot("Small Plot")}>Select</Button>
      </CardContent>
    </Card>

    <Card className="shadow-lg">
      <CardContent className="p-6 text-center">
        <h2 className="text-xl font-bold mb-2">Medium Plot</h2>
        <p className="mb-2">20 sq ft</p>
        <p className="text-green-600 font-bold mb-4">₹2,400 / 3 months</p>
        <Button onClick={() => setPlot("Medium Plot")}>Select</Button>
      </CardContent>
    </Card>

    <Card className="shadow-lg">
      <CardContent className="p-6 text-center">
        <h2 className="text-xl font-bold mb-2">Large Plot</h2>
        <p className="mb-2">40 sq ft</p>
        <p className="text-green-600 font-bold mb-4">₹4,800 / 3 months</p>
        <Button onClick={() => setPlot("Large Plot")}>Select</Button>
      </CardContent>
    </Card>
  </div>

  {/* Seasonal Veggie Chart */}
  <div className="max-w-4xl mx-auto py-12 px-4">
    <h2 className="text-2xl font-bold text-center mb-6">Seasonal Vegetables</h2>
    <div className="grid md:grid-cols-3 gap-4 text-center">
      <div className="bg-white p-4 rounded-2xl shadow">
        <h3 className="font-bold mb-2">Winter</h3>
        <p>Carrot, Spinach, Cauliflower, Peas</p>
      </div>
      <div className="bg-white p-4 rounded-2xl shadow">
        <h3 className="font-bold mb-2">Summer</h3>
        <p>Cucumber, Tomato, Beans, Okra</p>

