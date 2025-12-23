import React from 'react';
import { User, Mail, MapPin, Code, Database, Layout, Server, Flame } from 'lucide-react';

export default function FlutterDevReadme() {
  const languages = [
    { name: 'Dart', percentage: 45, color: '#0175C2' },
    { name: 'Java', percentage: 25, color: '#f89820' },
    { name: 'C++', percentage: 15, color: '#00599C' },
    { name: 'JavaScript', percentage: 10, color: '#F7DF1E' },
    { name: 'MySQL', percentage: 5, color: '#4479A1' }
  ];

  const stats = [
    { value: '150+', label: 'Total Contributions', sublabel: 'Past year' },
    { value: '12', label: 'Current Streak', sublabel: 'Days' },
    { value: '15', label: 'Public Repos', sublabel: 'Open Source' }
  ];

  const skills = {
    'Mobile Development': ['Flutter', 'Dart', 'Android', 'iOS'],
    'Backend': ['Java', 'PHP', 'Node.js'],
    'Database': ['MySQL', 'MongoDB', 'Firebase'],
    'Web': ['HTML', 'CSS', 'JavaScript', 'Bootstrap'],
    'Languages': ['C', 'C++', 'Java'],
    'Tools': ['Git', 'VS Code', 'Android Studio']
  };

  return (
    <div className="min-h-screen bg-gradient-to-br from-slate-50 to-blue-50 p-8">
      <div className="max-w-5xl mx-auto">
        {/* Header Card */}
        <div className="bg-white rounded-2xl shadow-lg p-8 mb-6 relative overflow-hidden">
          <div className="absolute top-0 right-0 w-64 h-64 bg-gradient-to-br from-blue-100 to-purple-100 rounded-full -mr-32 -mt-32 opacity-50"></div>
          
          <div className="relative flex items-start gap-6">
            <div className="w-32 h-32 bg-gradient-to-br from-blue-500 to-purple-600 rounded-full flex items-center justify-center text-white text-4xl font-bold shadow-lg">
              SD
            </div>
            
            <div className="flex-1">
              <div className="flex items-center gap-3 mb-2">
                <h1 className="text-4xl font-bold text-gray-800">Hey Everyone 👋, I'm Shivani Dhotre</h1>
              </div>
              
              <div className="inline-block bg-gradient-to-r from-blue-500 to-purple-600 text-white px-4 py-2 rounded-full text-sm font-semibold mb-4">
                FLUTTER DEV SPACE
              </div>
              
              <p className="text-gray-600 text-lg mb-4">
                A passionate <span className="font-semibold text-blue-600">Flutter Developer</span> from India 🇮🇳
              </p>
              
              <p className="text-gray-600 mb-4">
                I work on building beautiful cross-platform mobile applications. In my free time, I explore new technologies and contribute to open source projects.
              </p>
              
              <div className="flex flex-wrap gap-4 text-sm text-gray-600">
                <div className="flex items-center gap-2">
                  <MapPin size={16} className="text-blue-500" />
                  <span>India</span>
                </div>
                <div className="flex items-center gap-2">
                  <Mail size={16} className="text-blue-500" />
                  <span>shivanidhotre609@gmail.com</span>
                </div>
                <div className="flex items-center gap-2">
                  <User size={16} className="text-blue-500" />
                  <span>@shivanidhotre</span>
                </div>
              </div>
            </div>
          </div>
        </div>

        <div className="grid grid-cols-1 lg:grid-cols-3 gap-6 mb-6">
          {/* About Me Section */}
          <div className="lg:col-span-2 bg-white rounded-2xl shadow-lg p-6">
            <h2 className="text-2xl font-bold text-gray-800 mb-4 flex items-center gap-2">
              <Code className="text-blue-500" />
              About Me
            </h2>
            <ul className="space-y-3 text-gray-700">
              <li className="flex items-start gap-2">
                <span className="text-blue-500 mt-1">🔭</span>
                <span>I'm currently learning <strong>Flutter & Cross-Platform Development</strong></span>
              </li>
              <li className="flex items-start gap-2">
                <span className="text-blue-500 mt-1">📱</span>
                <span>All of my projects are available at <a href="https://github.com/shivanidhotre" className="text-blue-600 hover:underline">github.com/shivanidhotre</a></span>
              </li>
              <li className="flex items-start gap-2">
                <span className="text-blue-500 mt-1">💬</span>
                <span>Ask me about <strong>Flutter, Dart, Java, C++, Mobile Development</strong></span>
              </li>
              <li className="flex items-start gap-2">
                <span className="text-blue-500 mt-1">📫</span>
                <span>Reach me at <strong>shivanidhotre609@gmail.com</strong></span>
              </li>
            </ul>
          </div>

          {/* Stats Card */}
          <div className="bg-white rounded-2xl shadow-lg p-6">
            <h2 className="text-2xl font-bold text-gray-800 mb-4">GitHub Stats</h2>
            <div className="space-y-4">
              {stats.map((stat, index) => (
                <div key={index} className="text-center p-4 bg-gradient-to-br from-blue-50 to-purple-50 rounded-xl">
                  <div className="text-3xl font-bold text-blue-600">{stat.value}</div>
                  <div className="text-sm font-semibold text-gray-700">{stat.label}</div>
                  <div className="text-xs text-gray-500">{stat.sublabel}</div>
                </div>
              ))}
            </div>
          </div>
        </div>

        {/* Languages Card */}
        <div className="bg-white rounded-2xl shadow-lg p-6 mb-6">
          <h2 className="text-2xl font-bold text-gray-800 mb-4 flex items-center gap-2">
            <Flame className="text-orange-500" />
            Most Used Languages
          </h2>
          <div className="space-y-4">
            {languages.map((lang, index) => (
              <div key={index}>
                <div className="flex justify-between mb-1">
                  <span className="text-sm font-semibold text-gray-700">{lang.name}</span>
                  <span className="text-sm text-gray-600">{lang.percentage}%</span>
                </div>
                <div className="w-full bg-gray-200 rounded-full h-3 overflow-hidden">
                  <div 
                    className="h-full rounded-full transition-all duration-500"
                    style={{ 
                      width: `${lang.percentage}%`,
                      backgroundColor: lang.color
                    }}
                  ></div>
                </div>
              </div>
            ))}
          </div>
        </div>

        {/* Skills & Tools Grid */}
        <div className="bg-white rounded-2xl shadow-lg p-6 mb-6">
          <h2 className="text-2xl font-bold text-gray-800 mb-6 flex items-center gap-2">
            <Layout className="text-purple-500" />
            Languages & Tools
          </h2>
          <div className="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
            {Object.entries(skills).map(([category, items], index) => (
              <div key={index} className="bg-gradient-to-br from-blue-50 to-purple-50 rounded-xl p-4">
                <h3 className="font-bold text-gray-800 mb-3 flex items-center gap-2">
                  {category === 'Mobile Development' && <Server size={18} className="text-blue-500" />}
                  {category === 'Database' && <Database size={18} className="text-green-500" />}
                  {category}
                </h3>
                <div className="flex flex-wrap gap-2">
                  {items.map((skill, idx) => (
                    <span 
                      key={idx}
                      className="px-3 py-1 bg-white text-gray-700 rounded-full text-sm font-medium shadow-sm hover:shadow-md transition-shadow"
                    >
                      {skill}
                    </span>
                  ))}
                </div>
              </div>
            ))}
          </div>
        </div>

        {/* Connect Section */}
        <div className="bg-gradient-to-r from-blue-500 to-purple-600 rounded-2xl shadow-lg p-8 text-white text-center">
          <h2 className="text-3xl font-bold mb-4">Let's Connect! 🤝</h2>
          <p className="mb-6 text-blue-100">Feel free to reach out for collaborations or just a friendly chat</p>
          <div className="flex justify-center gap-4">
            <a 
              href="https://linkedin.com/in/shivani-dhotre-226046175" 
              className="px-6 py-3 bg-white text-blue-600 rounded-full font-semibold hover:bg-blue-50 transition-colors shadow-lg"
            >
              LinkedIn
            </a>
            <a 
              href="https://github.com/shivanidhotre" 
              className="px-6 py-3 bg-white text-purple-600 rounded-full font-semibold hover:bg-purple-50 transition-colors shadow-lg"
            >
              GitHub
            </a>
            <a 
              href="mailto:shivanidhotre609@gmail.com" 
              className="px-6 py-3 bg-white text-gray-800 rounded-full font-semibold hover:bg-gray-50 transition-colors shadow-lg"
            >
              Email
            </a>
          </div>
        </div>

        {/* Footer */}
        <div className="text-center mt-8 text-gray-600">
          <p className="text-sm">
            <img src="https://komarev.com/ghpvc/?username=shivanidhotre&label=Profile%20views&color=0e75b6&style=flat" alt="Profile views" className="inline" />
          </p>
        </div>
      </div>
    </div>
  );
}
