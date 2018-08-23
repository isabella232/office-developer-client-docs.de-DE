---
title: Dateiformat des Formulars Konfigurationsdateien
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 86e4ebd9-6df2-4346-9ce9-580f80a83884
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 95add2ca747a267b825648f0de82e8c8a83d3eb7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592255"
---
# <a name="file-format-of-form-configuration-files"></a>Dateiformat des Formulars Konfigurationsdateien

**Betrifft**: Outlook 2013 | Outlook 2016 
  
Eine Konfigurationsdatei Formular wird eine formatierte Datei, die Formularentwickler so definieren Sie ein Formular erstellt.
  
Da Formulardateien Konfiguration von Formular-Manager zum Laden von Formularen verwendet werden, muss jedes Formular mit einer Konfigurationsdatei Formular definiert werden. Konfigurationsdateien Formular müssen die cfg Filename-Erweiterung aufweisen. Die Datei befolgt die allgemeine Syntax von einer Windows-Initialisierungsdatei (INI-Datei). 

Es ist in benannte Abschnitte unterteilt, und jeder Abschnitt enthält eine Reihe von Einträge und Werte. Werte haben einen der folgenden Typen: Zeichenfolge, Zeichenfolge angezeigt, Plattformzeichenfolge, Pfad, Integer- oder globally unique Identifier, **GUID**. Formular Konfigurationsdateien können einen beliebigen Text-Editor oder Word-Prozessor, der die Textdateien speichern kann erstellt werden.
  

