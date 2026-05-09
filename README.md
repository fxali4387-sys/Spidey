# Spidey
export default function SpiderManAssembling() {
  const parts = [
    { name: 'Mask', emoji: '🕷️' },
    { name: 'Body Suit', emoji: '🟥' },
    { name: 'Gloves', emoji: '🧤' },
    { name: 'Boots', emoji: '👢' },
    { name: 'Web Shooter', emoji: '🕸️' },
  ];

  return (
    <div className="min-h-screen bg-gradient-to-b from-black via-red-900 to-blue-900 flex flex-col items-center justify-center p-6 text-white overflow-hidden">
      <h1 className="text-5xl md:text-7xl font-extrabold mb-4 text-center animate-pulse">
        Spider-Man Assembling
      </h1>

      <p className="text-lg md:text-2xl text-gray-200 mb-10 text-center max-w-2xl">
        Watch Spider-Man suit up piece by piece with cool glowing animations.
      </p>

      <div className="relative w-[320px] h-[520px] flex items-center justify-center">
        {/* Glow Background */}
        <div className="absolute w-72 h-72 bg-red-500 blur-3xl opacity-30 animate-pulse rounded-full"></div>

        {/* Spider-Man Body */}
        <div className="relative flex flex-col items-center gap-3 z-10">
          {parts.map((part, index) => (
            <div
              key={index}
              className="w-64 bg-white/10 backdrop-blur-md border border-white/20 rounded-3xl p-5 flex items-center justify-between shadow-2xl hover:scale-105 transition-transform duration-300 animate-bounce"
              style={{ animationDelay: `${index * 0.3}s` }}
            >
              <span className="text-2xl font-bold">{part.name}</span>
              <span className="text-4xl">{part.emoji}</span>
            </div>
          ))}
        </div>
      </div>

      <button className="mt-10 px-8 py-4 bg-red-600 hover:bg-red-700 rounded-2xl text-xl font-bold shadow-2xl hover:scale-110 transition-all duration-300">
        Assemble Now
      </button>

      <div className="absolute bottom-4 text-gray-300 text-sm tracking-widest animate-pulse">
        Friendly Neighborhood Spider-Man
      </div>
    </div>
  );
}
