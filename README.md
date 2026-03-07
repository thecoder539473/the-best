just so tuff
import React from 'react';
import { Shield, Activity, Thermometer } from 'lucide-react';

const HealthStatusCard = ({ patientName, status, temperature }) => {
  return (
    <div className="max-w-md mx-auto bg-white rounded-xl shadow-md overflow-hidden md:max-w-2xl border border-slate-200">
      <div className="p-8">
        <div className="uppercase tracking-wide text-sm text-indigo-500 font-semibold mb-1">
          Immune System Overview
        </div>
        <h2 className="block mt-1 text-lg leading-tight font-medium text-black">
          Patient: {patientName}
        </h2>
        
        <div className="mt-6 space-y-4">
          {/* Temperature Status */}
          <div className="flex items-center text-slate-600">
            <Thermometer className="mr-2 h-5 w-5 text-red-500" />
            <span>Body Temp: <span className="font-bold text-slate-900">{temperature}°F</span></span>
          </div>

          {/* Pathogen Defense Status */}
          <div className="flex items-center text-slate-600">
            <Shield className="mr-2 h-5 w-5 text-green-500" />
            <span>White Blood Cell Count: <span className="font-bold text-slate-900">Optimal</span></span>
          </div>

          {/* General Status */}
          <div className="flex items-center text-slate-600">
            <Activity className="mr-2 h-5 w-5 text-blue-500" />
            <span>Condition: <span className="italic">{status}</span></span>
          </div>
        </div>

        <button className="mt-6 w-full py-2 px-4 bg-indigo-600 text-white font-semibold rounded-lg shadow-md hover:bg-indigo-700 transition duration-200">
          Check Vaccination Records
        </button>
      </div>
    </div>
  );
};

export default HealthStatusCard;
