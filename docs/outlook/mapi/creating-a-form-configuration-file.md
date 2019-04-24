---
title: Erstellen einer Formular Konfigurationsdatei
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: aaf3b33d-ad2d-4ef8-847f-1ab1eaf08706
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 97ecafb2e4159c680fd23607f5ed6f8ea3156de7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32333019"
---
# <a name="creating-a-form-configuration-file"></a><span data-ttu-id="2dcd7-103">Erstellen einer Formular Konfigurationsdatei</span><span class="sxs-lookup"><span data-stu-id="2dcd7-103">Creating a Form Configuration File</span></span>

  
  
<span data-ttu-id="2dcd7-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2dcd7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2dcd7-105">Eine Formular Konfigurationsdatei enthält Informationen zu einem Formular sowohl für den verwendeten Formular-Manager als auch für Clientanwendungen.</span><span class="sxs-lookup"><span data-stu-id="2dcd7-105">A form configuration file provides information about a form both to the form manager being used and to client applications.</span></span> <span data-ttu-id="2dcd7-106">Eine Formular Konfigurationsdatei enthält eine umfangreiche Spezifikation für ein Formular, einschließlich der Eigenschaften, die vom Formular für die Verwendung durch Messagingclients veröffentlicht werden, die Verben, die vom Formular implementiert werden, und die vom Formular unterstützten Plattformen.</span><span class="sxs-lookup"><span data-stu-id="2dcd7-106">A form configuration file contains an extensive specification for a form, including the properties published by the form for use by messaging clients, the verbs implemented by the form, and the platforms supported by the form.</span></span>
  
<span data-ttu-id="2dcd7-107">Eine Formular Konfigurationsdatei ist eine Datei mit der Erweiterung. cfg und hat ein Format, das einer Windows-Initialisierungsdatei ähnelt.</span><span class="sxs-lookup"><span data-stu-id="2dcd7-107">A form configuration file is a file with a .cfg extension, and has a format similar to a Windows initialization file.</span></span> <span data-ttu-id="2dcd7-108">Es handelt sich um eine nur-Text-Datei mit einer Reihe von Abschnitten.</span><span class="sxs-lookup"><span data-stu-id="2dcd7-108">It is a plain text file with a number of sections.</span></span> <span data-ttu-id="2dcd7-109">Jeder Abschnitt beginnt mit einem Abschnittsnamen, der in eckigen Klammern eingeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="2dcd7-109">Each section begins with a section name, enclosed in square brackets.</span></span> <span data-ttu-id="2dcd7-110">Jeder Abschnitt enthält eine oder mehrere Zeilen, die Werte und Einstellungen für diesen Abschnitt definieren.</span><span class="sxs-lookup"><span data-stu-id="2dcd7-110">Each section contains one or more lines that define values and settings relevant to that section.</span></span> <span data-ttu-id="2dcd7-111">Werte haben einen der folgenden Typen:</span><span class="sxs-lookup"><span data-stu-id="2dcd7-111">Values have one of the following types:</span></span>
  
- <span data-ttu-id="2dcd7-112">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="2dcd7-112">String</span></span>
    
- <span data-ttu-id="2dcd7-113">Angezeigte Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="2dcd7-113">Displayed string</span></span>
    
- <span data-ttu-id="2dcd7-114">Plattformzeichenfolge</span><span class="sxs-lookup"><span data-stu-id="2dcd7-114">Platform string</span></span>
    
- <span data-ttu-id="2dcd7-115">Pfadname</span><span class="sxs-lookup"><span data-stu-id="2dcd7-115">Path name</span></span>
    
- <span data-ttu-id="2dcd7-116">Ganze Zahl</span><span class="sxs-lookup"><span data-stu-id="2dcd7-116">Integer</span></span>
    
- <span data-ttu-id="2dcd7-117">GUID</span><span class="sxs-lookup"><span data-stu-id="2dcd7-117">GUID</span></span>
    
<span data-ttu-id="2dcd7-118">Weitere Informationen zu den Abschnitten einer cfg-Datei finden Sie unter [File Format of Form Configuration Files](file-format-of-form-configuration-files.md).</span><span class="sxs-lookup"><span data-stu-id="2dcd7-118">For more information about the sections of a .cfg file, see [File Format of Form Configuration Files](file-format-of-form-configuration-files.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="2dcd7-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2dcd7-119">See also</span></span>



[<span data-ttu-id="2dcd7-120">Entwickeln von MAPI-Formular Servern</span><span class="sxs-lookup"><span data-stu-id="2dcd7-120">Developing MAPI Form Servers</span></span>](developing-mapi-form-servers.md)

