# F.Gestalt
Architecture designs and procurement products 
import { Card, CardContent } from "@/components/ui/card";
import { Button } from "@/components/ui/button";
import { useState } from "react";

export default function Home() {
  const [shopItems] = useState([
    { name: "Deco Item", price: "$45", image: "/placeholder-deco.jpg" },
    { name: "Flexible Chair", price: "$120", image: "/placeholder-chair.jpg" },
    { name: "Vinyl Flooring", price: "$60", image: "/placeholder-floor.jpg" },
    { name: "Room Partition", price: "$80", image: "/placeholder-partition.jpg" },
  ]);

  return (
    <div className="p-6 space-y-10">
      <header className="text-center">
        <h1 className="text-4xl font-bold">F. Gestalt</h1>
        <p className="text-lg text-muted-foreground mt-2">
          Architecture. Design. Interiors.
      

      <section className="text-center">
        <h2 className="text-2xl font-semibold mb-4">About</h2>
        <p className="max-w-2xl mx-auto">
          Francisca Nana Adwoa Saah is a Ghana-based architect and interior designer.
          Through F. Gestalt, she brings storytelling, emotion, and spatial innovation
          to life. With international experience and award-nominated projects like The Ruby,
          her work is rooted in function and inspired by form.
        </p>
      </section>

      <section>
        <h2 className="text-2xl font-semibold mb-4 text-center">Selected Works</h2>
        <div className="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 gap-6">
          <Card>
            <CardContent className="p-4">
              <img src="/middle-income-housing.jpg" alt="Middle Income Housing" className="rounded-xl mb-2" />
              <h3 className="font-bold">Middle Income Housing – Ahodwo</h3>
              <p className="text-sm text-muted-foreground">Academic Project</p>
            </CardContent>
          </Card>
          <Card>
            <CardContent className="p-4">
              <img src="/the-ruby.jpg" alt="The Ruby" className="rounded-xl mb-2" />
              <h3 className="font-bold">The Ruby – Cantonments</h3>
              <p className="text-sm text-muted-foreground">Professional Project</p>
            </CardContent>
          </Card>
          <Card>
            <CardContent className="p-4">
              <img src="/bubbil-laundromat.jpg" alt="Bubbil Laundromat" className="rounded-xl mb-2" />
              <h3 className="font-bold">Bubbil Laundromat</h3>
              <p className="text-sm text-muted-foreground">Modular Design</p>
            </CardContent>
          </Card>
        </div>
      </section>

      <section>
        <h2 className="text-2xl font-semibold mb-4 text-center">Shop Interior Pieces</h2>
        <div className="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-4 gap-6">
          {shopItems.map((item, i) => (
            <Card key={i}>
              <CardContent className="p-4">
                <img src={item.image} alt={item.name} className="rounded-xl mb-2" />
                <h3 className="font-semibold">{item.name}</h3>
                <p className="text-sm text-muted-foreground">{item.price}</p>
                <Button className="mt-2 w-full">Add to Cart</Button>
              </CardContent>
            </Card>
          ))}
        </div>
      </section>

      <footer className="text-center text-sm text-muted-foreground mt-10">
        Contact: saahfranca4@gmail.com | +233 459 826 800 / +233 508 624 108
      </footer>
    </div>
  );
}
