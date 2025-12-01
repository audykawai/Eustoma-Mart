import { Card, CardContent } from "@/components/ui/card";
import { Button } from "@/components/ui/button";
import { Mail, Instagram, MapPin, ShoppingBag } from "lucide-react";

export default function Page() {
  const newProducts = [
    { name: "Tisu", price: 6000 },
    { name: "Air Mineral", price: 5000 },
    { name: "Biskuit", price: 8000 },
    { name: "Sandal", price: 20000 },
    { name: "Sabun Cuci Piring", price: 10000 }
  ];

  const otherProducts = [
  { name: "Lem Kertas", price: 11250 },
  { name: "Stopmap", price: 16875 },
  { name: "Perlak Bayi", price: 22500 },
  { name: "Mangkuk", price: 9000 },
  { name: "Cangkir", price: 5625 },
  { name: "Sarung Tangan", price: 16875 },
  { name: "Sampo Neril", price: 45000 },
  { name: "Sampo Pantene", price: 38250 },
  { name: "Pembersih Jelita", price: 18000 },
  { name: "Penyegar Jelita", price: 14625 },
  { name: "Bedak Jelita", price: 15750 },
  { name: "Alas Bedak Jelita", price: 12375 },
  { name: "Parfum Volare", price: 45000 },
  { name: "Roti Sisir Matahari", price: 13500 },
  { name: "Roti Tawar Francisco", price: 11250 },
  { name: "Margarin Lezat", price: 4500 },
  { name: "Margarin Lofat", price: 4500 },
  { name: "Sari Apel Manalagi", price: 5625 },
  { name: "Sinom Fress", price: 5625 },
  { name: "Teh Kotak Fren", price: 4500 }
];

  return (
    <div className="min-h-screen bg-[#E9F2FF] text-blue-900 p-6 flex justify-center">
      <div className="max-w-5xl w-full space-y-6">

        {/* HEADER */}
        <div className="text-center space-y-2">
          <h1 className="text-4xl font-bold">Eustoma Mart</h1>
          <p className="text-xl opacity-80">Solusi Belanja Cepat & Terpercaya</p>
        </div>

        {/* CONTACT SECTION */}
        <Card className="border-none shadow-lg rounded-2xl">
          <CardContent className="p-4 grid sm:grid-cols-3 gap-4 text-center">
            <div className="flex items-center justify-center gap-2">
              <Instagram className="w-6 h-6" /> <span>@eustomamart</span>
            </div>
            <div className="flex items-center justify-center gap-2">
              <Mail className="w-6 h-6" /> <span>Eustoma@bisnis.ukwms.ac.id</span>
            </div>
            <div className="flex items-center justify-center gap-2">
              <MapPin className="w-6 h-6" /> <span>Jalan Garuda No. 50, Surabaya</span>
            </div>
          </CardContent>
        </Card>

        {/* NEW PRODUCTS */}
        <div>
          <h2 className="text-2xl font-semibold flex items-center gap-2 mb-4">
            <ShoppingBag className="w-6 h-6" /> Produk Baru
          </h2>
          <div className="grid sm:grid-cols-2 lg:grid-cols-5 gap-4">
            {newProducts.map((p, i) => (
              <Card key={i} className="border-none shadow-md rounded-2xl hover:scale-105 transition">
                <CardContent className="p-4 text-center">
                  <ShoppingBag className="mx-auto w-5 h-5 mb-2 opacity-70" />
                  <p className="font-medium">{p.name}</p>
                  <p className="text-blue-600 font-bold">Rp {p.price.toLocaleString()}</p>
                </CardContent>
              </Card>
            ))}
          </div>
        </div>

        {/* OTHER PRODUCTS FROM IMAGE */}
        <div>
          <h2 className="text-2xl font-semibold flex items-center gap-2 mb-4">
            <ShoppingBag className="w-6 h-6" /> Produk Lainnya
          </h2>
          <div className="grid sm:grid-cols-2 lg:grid-cols-4 gap-4">
            {otherProducts.map((p, i) => (
              <Card key={i} className="border-none shadow-md rounded-2xl hover:scale-105 transition">
                <CardContent className="p-4 space-y-1">
                  <div className="flex justify-center mb-2 opacity-60"><ShoppingBag className="w-5 h-5" /></div>
                  <p className="font-semibold text-center">{p.name}</p>
                  <p className="text-sm text-center opacity-80">{p.supplier}</p>
                  <p className="text-blue-600 font-bold text-center">Rp {Number(p.price).toLocaleString()}</p>
                </CardContent>
              </Card>
            ))}
          </div>
        </div>

        {/* ORDER INFO */}
        <Card className="border-none shadow-lg rounded-2xl bg-white">
          <CardContent className="p-5 text-center space-y-2">
            <h2 className="text-xl font-bold flex items-center justify-center gap-2"><ShoppingBag /> Cara Pemesanan</h2>
            <p>Datang langsung ke toko atau pesan lewat Gmail kami.</p>
            <Button className="rounded-xl shadow">Pesan via Gmail</Button>
          </CardContent>
        </Card>

      </div>
    </div>
  );
}
