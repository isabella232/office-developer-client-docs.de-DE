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
# <a name="file-format-of-form-configuration-files"></a><span data-ttu-id="cdf21-103">Dateiformat des Formulars Konfigurationsdateien</span><span class="sxs-lookup"><span data-stu-id="cdf21-103">File format of form configuration files</span></span>

<span data-ttu-id="cdf21-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cdf21-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cdf21-105">Eine Konfigurationsdatei Formular wird eine formatierte Datei, die Formularentwickler so definieren Sie ein Formular erstellt.</span><span class="sxs-lookup"><span data-stu-id="cdf21-105">A form configuration file is a formatted file created by form developers to define a form.</span></span>
  
<span data-ttu-id="cdf21-106">Da Formulardateien Konfiguration von Formular-Manager zum Laden von Formularen verwendet werden, muss jedes Formular mit einer Konfigurationsdatei Formular definiert werden.</span><span class="sxs-lookup"><span data-stu-id="cdf21-106">Because form configuration files are used by form managers to load forms, each form must be defined using a form configuration file.</span></span> <span data-ttu-id="cdf21-107">Konfigurationsdateien Formular müssen die cfg Filename-Erweiterung aufweisen.</span><span class="sxs-lookup"><span data-stu-id="cdf21-107">Form configuration files must have the .cfg filename extension.</span></span> <span data-ttu-id="cdf21-108">Die Datei befolgt die allgemeine Syntax von einer Windows-Initialisierungsdatei (INI-Datei).</span><span class="sxs-lookup"><span data-stu-id="cdf21-108">The file follows the general syntax of a Windows initialization file (.ini file).</span></span> 

<span data-ttu-id="cdf21-109">Es ist in benannte Abschnitte unterteilt, und jeder Abschnitt enthält eine Reihe von Einträge und Werte.</span><span class="sxs-lookup"><span data-stu-id="cdf21-109">It is divided into named sections, and each section contains a series of entries and values.</span></span> <span data-ttu-id="cdf21-110">Werte haben einen der folgenden Typen: Zeichenfolge, Zeichenfolge angezeigt, Plattformzeichenfolge, Pfad, Integer- oder globally unique Identifier, **GUID**.</span><span class="sxs-lookup"><span data-stu-id="cdf21-110">Values have one of the following types: string, displayed string, platform string, path, integer, or globally unique identifier, **GUID**.</span></span> <span data-ttu-id="cdf21-111">Formular Konfigurationsdateien können einen beliebigen Text-Editor oder Word-Prozessor, der die Textdateien speichern kann erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="cdf21-111">Form configuration files can be created with any text editor or word processor that is capable of saving text files.</span></span>
  

