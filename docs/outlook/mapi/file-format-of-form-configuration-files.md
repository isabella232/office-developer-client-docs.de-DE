---
title: Dateiformat von Formularkonfigurationsdateien
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 86e4ebd9-6df2-4346-9ce9-580f80a83884
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 06265db7486da3e112712a079adc3348f3be3a58
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59588042"
---
# <a name="file-format-of-form-configuration-files"></a>Dateiformat von Formularkonfigurationsdateien

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Eine Formularkonfigurationsdatei ist eine formatierte Datei, die von Formularentwicklern zum Definieren eines Formulars erstellt wurde.
  
Da Formularkonfigurationsdateien von Formularmanagern zum Laden von Formularen verwendet werden, muss jedes Formular mithilfe einer Formularkonfigurationsdatei definiert werden. Formularkonfigurationsdateien müssen die Dateinamenerweiterung CFG aufweisen. Die Datei folgt der allgemeinen Syntax einer Windows Initialisierungsdatei (.ini-Datei). 

Er ist in benannte Abschnitte unterteilt, und jeder Abschnitt enthält eine Reihe von Einträgen und Werten. Werte haben einen der folgenden Typen: Zeichenfolge, angezeigte Zeichenfolge, Plattformzeichenfolge, Pfad, ganze Zahl oder global eindeutiger Bezeichner, **GUID.** Formularkonfigurationsdateien können mit einem beliebigen Text-Editor oder Textverarbeitungsprogramm erstellt werden, der Textdateien speichern kann.
  

