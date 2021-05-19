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
# <a name="file-format-of-form-configuration-files"></a><span data-ttu-id="e3f88-103">Dateiformat von Formularkonfigurationsdateien</span><span class="sxs-lookup"><span data-stu-id="e3f88-103">File format of form configuration files</span></span>

<span data-ttu-id="e3f88-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e3f88-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e3f88-105">Eine Formularkonfigurationsdatei ist eine formatierte Datei, die von Formularentwicklern zum Definieren eines Formulars erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="e3f88-105">A form configuration file is a formatted file created by form developers to define a form.</span></span>
  
<span data-ttu-id="e3f88-106">Da Formularkonfigurationsdateien von Formularmanagern zum Laden von Formularen verwendet werden, muss jedes Formular mithilfe einer Formularkonfigurationsdatei definiert werden.</span><span class="sxs-lookup"><span data-stu-id="e3f88-106">Because form configuration files are used by form managers to load forms, each form must be defined using a form configuration file.</span></span> <span data-ttu-id="e3f88-107">Formularkonfigurationsdateien müssen die Dateinamenerweiterung .cfg haben.</span><span class="sxs-lookup"><span data-stu-id="e3f88-107">Form configuration files must have the .cfg filename extension.</span></span> <span data-ttu-id="e3f88-108">Die Datei folgt der allgemeinen Syntax einer Windows Initialisierungsdatei (.ini Datei).</span><span class="sxs-lookup"><span data-stu-id="e3f88-108">The file follows the general syntax of a Windows initialization file (.ini file).</span></span> 

<span data-ttu-id="e3f88-109">Er ist in benannte Abschnitte unterteilt, und jeder Abschnitt enthält eine Reihe von Einträgen und Werten.</span><span class="sxs-lookup"><span data-stu-id="e3f88-109">It is divided into named sections, and each section contains a series of entries and values.</span></span> <span data-ttu-id="e3f88-110">Werte haben einen der folgenden Typen: Zeichenfolge, angezeigte Zeichenfolge, Plattformzeichenfolge, Pfad, ganzzahlige oder global eindeutige **ID, GUID**.</span><span class="sxs-lookup"><span data-stu-id="e3f88-110">Values have one of the following types: string, displayed string, platform string, path, integer, or globally unique identifier, **GUID**.</span></span> <span data-ttu-id="e3f88-111">Formularkonfigurationsdateien können mit jedem Beliebigen Texteditor oder Textprozessor erstellt werden, der Textdateien speichern kann.</span><span class="sxs-lookup"><span data-stu-id="e3f88-111">Form configuration files can be created with any text editor or word processor that is capable of saving text files.</span></span>
  

