---
title: Dateiformat des Formulars Konfigurationsdateien
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 86e4ebd9-6df2-4346-9ce9-580f80a83884
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: def91b4e28e60f6d2e8534f0ed7261777ec0c8e0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791667"
---
# <a name="file-format-of-form-configuration-files"></a>Dateiformat des Formulars Konfigurationsdateien

**Betrifft**: Outlook 
  
Eine Konfigurationsdatei Formular wird eine formatierte Datei, die Formularentwickler so definieren Sie ein Formular erstellt.
  
Da Formulardateien Konfiguration von Formular-Manager zum Laden von Formularen verwendet werden, muss jedes Formular mit einer Konfigurationsdatei Formular definiert werden. Konfigurationsdateien Formular müssen die cfg Filename-Erweiterung aufweisen. Die Datei befolgt die allgemeine Syntax von einer Windows-Initialisierungsdatei (INI-Datei). 

Es ist in benannte Abschnitte unterteilt, und jeder Abschnitt enthält eine Reihe von Einträge und Werte. Werte haben einen der folgenden Typen: Zeichenfolge, Zeichenfolge angezeigt, Plattformzeichenfolge, Pfad, Integer- oder globally unique Identifier, **GUID**. Formular Konfigurationsdateien können einen beliebigen Text-Editor oder Word-Prozessor, der die Textdateien speichern kann erstellt werden.
  

