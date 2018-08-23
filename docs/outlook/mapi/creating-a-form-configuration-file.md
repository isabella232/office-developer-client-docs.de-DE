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
ms.openlocfilehash: d8159d93aef020d7c9c1b56be4cf6256f80b8aa3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584168"
---
# <a name="creating-a-form-configuration-file"></a><span data-ttu-id="7aedc-103">Erstellen einer Formularkonfigurationsdatei</span><span class="sxs-lookup"><span data-stu-id="7aedc-103">Creating a Form Configuration File</span></span>

  
  
<span data-ttu-id="7aedc-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7aedc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7aedc-105">Eine Konfigurationsdatei Formular enthält Informationen zu einem Formular, an den Formular-Manager verwendeten und Clientanwendungen.</span><span class="sxs-lookup"><span data-stu-id="7aedc-105">A form configuration file provides information about a form both to the form manager being used and to client applications.</span></span> <span data-ttu-id="7aedc-106">Eine Konfigurationsdatei Formular enthält eine umfassende Spezifikation für ein Formular, einschließlich der Eigenschaften, die vom Formular für die Verwendung von messaging-Clients, die vom Formular implementierte Verben und die Plattformen, die vom Formular veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="7aedc-106">A form configuration file contains an extensive specification for a form, including the properties published by the form for use by messaging clients, the verbs implemented by the form, and the platforms supported by the form.</span></span>
  
<span data-ttu-id="7aedc-107">Eine Konfigurationsdatei Formular ist eine Datei mit der Erweiterung cfg und weist das Format einer Windows-Initialisierungsdatei ähnelt.</span><span class="sxs-lookup"><span data-stu-id="7aedc-107">A form configuration file is a file with a .cfg extension, and has a format similar to a Windows initialization file.</span></span> <span data-ttu-id="7aedc-108">Es handelt sich um eine nur-Text-Datei mit einer Anzahl von Abschnitten.</span><span class="sxs-lookup"><span data-stu-id="7aedc-108">It is a plain text file with a number of sections.</span></span> <span data-ttu-id="7aedc-109">Jeder Abschnitt beginnt mit einem Abschnittsnamen, die in Klammern eingeschlossen.</span><span class="sxs-lookup"><span data-stu-id="7aedc-109">Each section begins with a section name, enclosed in square brackets.</span></span> <span data-ttu-id="7aedc-110">Jeder Abschnitt enthält eine oder mehrere Zeilen, die Werte und Einstellungen für diesen Abschnitt relevant definieren.</span><span class="sxs-lookup"><span data-stu-id="7aedc-110">Each section contains one or more lines that define values and settings relevant to that section.</span></span> <span data-ttu-id="7aedc-111">Werte haben einen der folgenden Typen:</span><span class="sxs-lookup"><span data-stu-id="7aedc-111">Values have one of the following types:</span></span>
  
- <span data-ttu-id="7aedc-112">String</span><span class="sxs-lookup"><span data-stu-id="7aedc-112">String</span></span>
    
- <span data-ttu-id="7aedc-113">Zeichenfolge angezeigt</span><span class="sxs-lookup"><span data-stu-id="7aedc-113">Displayed string</span></span>
    
- <span data-ttu-id="7aedc-114">Plattformzeichenfolge</span><span class="sxs-lookup"><span data-stu-id="7aedc-114">Platform string</span></span>
    
- <span data-ttu-id="7aedc-115">Pfadname</span><span class="sxs-lookup"><span data-stu-id="7aedc-115">Path name</span></span>
    
- <span data-ttu-id="7aedc-116">Ganze Zahl</span><span class="sxs-lookup"><span data-stu-id="7aedc-116">Integer</span></span>
    
- <span data-ttu-id="7aedc-117">GUID</span><span class="sxs-lookup"><span data-stu-id="7aedc-117">GUID</span></span>
    
<span data-ttu-id="7aedc-118">Weitere Informationen zu den Abschnitten einer Datei CFG finden Sie unter [File Format des Formulars Konfigurationsdateien](file-format-of-form-configuration-files.md).</span><span class="sxs-lookup"><span data-stu-id="7aedc-118">For more information about the sections of a .cfg file, see [File Format of Form Configuration Files](file-format-of-form-configuration-files.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="7aedc-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7aedc-119">See also</span></span>



[<span data-ttu-id="7aedc-120">Entwickeln von MAPI-Formularservern</span><span class="sxs-lookup"><span data-stu-id="7aedc-120">Developing MAPI Form Servers</span></span>](developing-mapi-form-servers.md)

