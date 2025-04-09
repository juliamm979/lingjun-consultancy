# lingjun-consultancy
Lingjun Consultancy Official Website
import React from "react";
import { useTranslation } from "react-i18next";
import i18n from "./i18n";
import "./index.css";

const App = () => {
  const { t } = useTranslation();

  const changeLanguage = (lng) => {
    i18n.changeLanguage(lng);
  };

  return (
    <div className="min-h-screen flex flex-col items-center justify-center bg-white text-gray-800 p-4">
      <div className="flex space-x-4 mb-6">
        <button onClick={() => changeLanguage("en")} className="bg-orange-500 text-white px-4 py-2 rounded">EN</button>
        <button onClick={() => changeLanguage("zh")} className="bg-yellow-500 text-white px-4 py-2 rounded">中文</button>
      </div>
      <h1 className="text-4xl font-bold mb-4">{t("welcome")}</h1>
      <p className="text-lg">{t("tagline")}</p>
    </div>
  );
};

export default App;
