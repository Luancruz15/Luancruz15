import React from 'react';
import { CircleUserRound, Star, GitFork, MessageSquare, AlertCircle, Users, Code2 } from 'lucide-react';

function App() {
  return (
    <div className="min-h-screen bg-[#0d1117] text-gray-200 p-8">
      <div className="max-w-4xl mx-auto">
        <div className="mb-8">
          <h1 className="text-2xl font-bold text-purple-500 mb-6">Your GitHub Stats</h1>
          
          {/* Stats Grid */}
          <div className="grid grid-cols-1 md:grid-cols-2 gap-6">
            {/* Left Column - Stats */}
            <div className="space-y-4">
              <div className="flex items-center space-x-3">
                <Star className="text-purple-500" size={20} />
                <span className="text-gray-400">Total Stars Earned:</span>
                <span className="text-purple-500 font-semibold">203</span>
              </div>
              
              <div className="flex items-center space-x-3">
                <Code2 className="text-purple-500" size={20} />
                <span className="text-gray-400">Total Commits (2025):</span>
                <span className="text-purple-500 font-semibold">925</span>
              </div>
              
              <div className="flex items-center space-x-3">
                <GitFork className="text-purple-500" size={20} />
                <span className="text-gray-400">Total PRs:</span>
                <span className="text-purple-500 font-semibold">2</span>
              </div>
              
              <div className="flex items-center space-x-3">
                <AlertCircle className="text-purple-500" size={20} />
                <span className="text-gray-400">Total Issues:</span>
                <span className="text-purple-500 font-semibold">1</span>
              </div>
              
              <div className="flex items-center space-x-3">
                <Users className="text-purple-500" size={20} />
                <span className="text-gray-400">Contributed to (last year):</span>
                <span className="text-purple-500 font-semibold">0</span>
              </div>
            </div>
            
            {/* Right Column - Grade and Languages */}
            <div>
              {/* Grade Circle */}
              <div className="flex justify-center mb-6">
                <div className="w-32 h-32 rounded-full border-4 border-purple-500 flex items-center justify-center">
                  <span className="text-4xl font-bold text-purple-500">B+</span>
                </div>
              </div>
              
              {/* Languages */}
              <div className="space-y-3">
                <h2 className="text-xl font-semibold text-purple-500 mb-4">Most Used Languages</h2>
                
                <div className="space-y-2">
                  <LanguageBar name="JavaScript" percentage={27.41} color="bg-yellow-400" />
                  <LanguageBar name="HTML" percentage={23.01} color="bg-orange-500" />
                  <LanguageBar name="Python" percentage={19.56} color="bg-blue-400" />
                  <LanguageBar name="CSS" percentage={15.46} color="bg-purple-400" />
                  <LanguageBar name="Java" percentage={9.37} color="bg-yellow-600" />
                  <LanguageBar name="Portugol" percentage={3.49} color="bg-yellow-500" />
                  <LanguageBar name="Jupyter Notebook" percentage={1.70} color="bg-orange-400" />
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  );
}

function LanguageBar({ name, percentage, color }: { name: string; percentage: number; color: string }) {
  return (
    <div className="space-y-1">
      <div className="flex justify-between text-sm">
        <span>{name}</span>
        <span>{percentage}%</span>
      </div>
      <div className="h-2 bg-gray-700 rounded-full overflow-hidden">
        <div 
          className={`h-full ${color} rounded-full`} 
          style={{ width: `${percentage}%` }}
        />
      </div>
    </div>
  );
}

export default App;
