# Neptune-Launchpad
A platform for creatives to build professional profiles, access tools and mentorship, run campaigns, collaborate, and monetize their work.
import React, { useState } from "react";

function Dashboard() {
  return (
    <div className="p-8">
      <h2 className="text-2xl font-bold mb-4">Welcome to Your Dashboard!</h2>
      <p>This is where your creative tools and features will appear.</p>
    </div>
  );
}

export default function CreativeLaunchApp() {
  const [started, setStarted] = useState(false);

  return (
    <div className="min-h-screen flex flex-col items-center justify-center p-8 bg-gradient-to-br from-blue-100 to-purple-200">
      {!started ? (
        <>
          <h1 className="text-4xl font-bold mb-4 text-center">Welcome to CreativeLaunch</h1>
          <p className="text-lg text-center max-w-xl mb-6">
            Empowering creatives through digital tools, mentorship, and collaboration.
          </p>
          <button
            onClick={() => setStarted(true)}
            className="bg-blue-600 text-white px-6 py-2 rounded-lg hover:bg-blue-700 transition"
          >
            Get Started
          </button>
        </>
      ) : (
        <Dashboard />
      )}
    </div>
  );
}
