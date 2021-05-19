---
title: Erstellen einer Formularkonfigurationsdatei
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: aaf3b33d-ad2d-4ef8-847f-1ab1eaf08706
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 97ecafb2e4159c680fd23607f5ed6f8ea3156de7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425218"
---
# <a name="creating-a-form-configuration-file"></a><span data-ttu-id="c001b-103">Erstellen einer Formularkonfigurationsdatei</span><span class="sxs-lookup"><span data-stu-id="c001b-103">Creating a Form Configuration File</span></span>

  
  
<span data-ttu-id="c001b-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c001b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c001b-105">Eine Formularkonfigurationsdatei enthält Informationen zu einem Formular sowohl für den verwendeten Formular-Manager als auch für Clientanwendungen.</span><span class="sxs-lookup"><span data-stu-id="c001b-105">A form configuration file provides information about a form both to the form manager being used and to client applications.</span></span> <span data-ttu-id="c001b-106">Eine Formularkonfigurationsdatei enthält eine umfassende Spezifikation für ein Formular, einschließlich der vom Formular veröffentlichten Eigenschaften für die Verwendung durch Messagingclients, der vom Formular implementierten Verben und der vom Formular unterstützten Plattformen.</span><span class="sxs-lookup"><span data-stu-id="c001b-106">A form configuration file contains an extensive specification for a form, including the properties published by the form for use by messaging clients, the verbs implemented by the form, and the platforms supported by the form.</span></span>
  
<span data-ttu-id="c001b-107">Eine Formularkonfigurationsdatei ist eine Datei mit einer CFG-Erweiterung und hat ein Format, das einer Windows ist.</span><span class="sxs-lookup"><span data-stu-id="c001b-107">A form configuration file is a file with a .cfg extension, and has a format similar to a Windows initialization file.</span></span> <span data-ttu-id="c001b-108">Es handelt sich um eine Nur-Text-Datei mit einer Reihe von Abschnitten.</span><span class="sxs-lookup"><span data-stu-id="c001b-108">It is a plain text file with a number of sections.</span></span> <span data-ttu-id="c001b-109">Jeder Abschnitt beginnt mit einem Abschnittsnamen, der in eckige Klammern eingeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="c001b-109">Each section begins with a section name, enclosed in square brackets.</span></span> <span data-ttu-id="c001b-110">Jeder Abschnitt enthält eine oder mehrere Zeilen, die Werte und Einstellungen definieren, die für diesen Abschnitt relevant sind.</span><span class="sxs-lookup"><span data-stu-id="c001b-110">Each section contains one or more lines that define values and settings relevant to that section.</span></span> <span data-ttu-id="c001b-111">Werte haben einen der folgenden Typen:</span><span class="sxs-lookup"><span data-stu-id="c001b-111">Values have one of the following types:</span></span>
  
- <span data-ttu-id="c001b-112">String</span><span class="sxs-lookup"><span data-stu-id="c001b-112">String</span></span>
    
- <span data-ttu-id="c001b-113">Angezeigte Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="c001b-113">Displayed string</span></span>
    
- <span data-ttu-id="c001b-114">Plattformzeichenfolge</span><span class="sxs-lookup"><span data-stu-id="c001b-114">Platform string</span></span>
    
- <span data-ttu-id="c001b-115">Pfadname</span><span class="sxs-lookup"><span data-stu-id="c001b-115">Path name</span></span>
    
- <span data-ttu-id="c001b-116">Ganze Zahl</span><span class="sxs-lookup"><span data-stu-id="c001b-116">Integer</span></span>
    
- <span data-ttu-id="c001b-117">GUID</span><span class="sxs-lookup"><span data-stu-id="c001b-117">GUID</span></span>
    
<span data-ttu-id="c001b-118">Weitere Informationen zu den Abschnitten einer CFG-Datei finden Sie unter [Dateiformat von Formularkonfigurationsdateien](file-format-of-form-configuration-files.md).</span><span class="sxs-lookup"><span data-stu-id="c001b-118">For more information about the sections of a .cfg file, see [File Format of Form Configuration Files](file-format-of-form-configuration-files.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c001b-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c001b-119">See also</span></span>



[<span data-ttu-id="c001b-120">Entwickeln von MAPI-Formularservern</span><span class="sxs-lookup"><span data-stu-id="c001b-120">Developing MAPI Form Servers</span></span>](developing-mapi-form-servers.md)

