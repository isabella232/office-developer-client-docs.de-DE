---
title: Dateiformat von Formularkonfigurationsdateien
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 86e4ebd9-6df2-4346-9ce9-580f80a83884
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: d07d88d7b8b892a82832f91989e322ea3b32e040
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415551"
---
# <a name="file-format-of-form-configuration-files"></a>Dateiformat von Formularkonfigurationsdateien

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Eine Formular Konfigurationsdatei ist eine formatierte Datei, die von Formularentwicklern erstellt wurde, um ein Formular zu definieren.
  
Da Formular Konfigurationsdateien von Formular Managern zum Laden von Formularen verwendet werden, muss jedes Formular mithilfe einer Formular Konfigurationsdatei definiert werden. Formular Konfigurationsdateien müssen die Dateinamenerweiterung cfg aufweisen. Die Datei folgt der allgemeinen Syntax einer Windows-Initialisierungsdatei (INI-Datei). 

Sie ist in benannte Abschnitte unterteilt, und jeder Abschnitt enthält eine Reihe von Einträgen und Werten. Werte haben einen der folgenden Typen: Zeichenfolge, angezeigte Zeichenfolge, Plattformzeichenfolge, Pfad, ganze Zahl oder global eindeutiger Bezeichner, **GUID**. Formular Konfigurationsdateien können mit einem beliebigen Text-Editor oder einem Textverarbeitungsprogramm erstellt werden, das Textdateien speichern kann.
  

