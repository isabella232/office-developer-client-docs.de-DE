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
# <a name="file-format-of-form-configuration-files"></a><span data-ttu-id="7a226-103">Dateiformat des Formulars Konfigurationsdateien</span><span class="sxs-lookup"><span data-stu-id="7a226-103">File format of form configuration files</span></span>

<span data-ttu-id="7a226-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7a226-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7a226-105">Eine Konfigurationsdatei Formular wird eine formatierte Datei, die Formularentwickler so definieren Sie ein Formular erstellt.</span><span class="sxs-lookup"><span data-stu-id="7a226-105">A form configuration file is a formatted file created by form developers to define a form.</span></span>
  
<span data-ttu-id="7a226-106">Da Formulardateien Konfiguration von Formular-Manager zum Laden von Formularen verwendet werden, muss jedes Formular mit einer Konfigurationsdatei Formular definiert werden.</span><span class="sxs-lookup"><span data-stu-id="7a226-106">Because form configuration files are used by form managers to load forms, each form must be defined using a form configuration file.</span></span> <span data-ttu-id="7a226-107">Konfigurationsdateien Formular müssen die cfg Filename-Erweiterung aufweisen.</span><span class="sxs-lookup"><span data-stu-id="7a226-107">Form configuration files must have the .cfg filename extension.</span></span> <span data-ttu-id="7a226-108">Die Datei befolgt die allgemeine Syntax von einer Windows-Initialisierungsdatei (INI-Datei).</span><span class="sxs-lookup"><span data-stu-id="7a226-108">The file follows the general syntax of a Windows initialization file (.ini file).</span></span> 

<span data-ttu-id="7a226-109">Es ist in benannte Abschnitte unterteilt, und jeder Abschnitt enthält eine Reihe von Einträge und Werte.</span><span class="sxs-lookup"><span data-stu-id="7a226-109">It is divided into named sections, and each section contains a series of entries and values.</span></span> <span data-ttu-id="7a226-110">Werte haben einen der folgenden Typen: Zeichenfolge, Zeichenfolge angezeigt, Plattformzeichenfolge, Pfad, Integer- oder globally unique Identifier, **GUID**.</span><span class="sxs-lookup"><span data-stu-id="7a226-110">Values have one of the following types: string, displayed string, platform string, path, integer, or globally unique identifier, **GUID**.</span></span> <span data-ttu-id="7a226-111">Formular Konfigurationsdateien können einen beliebigen Text-Editor oder Word-Prozessor, der die Textdateien speichern kann erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="7a226-111">Form configuration files can be created with any text editor or word processor that is capable of saving text files.</span></span>
  

