---
title: Abschnitt "MapiSvc. inf [Services]"
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 99f8e623-3138-4def-9778-5580326111a5
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: e5bf5242ef673976ebda928d6ce4862e3e7dd072
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434781"
---
# <a name="mapisvcinf-services-section"></a><span data-ttu-id="e03ac-103">Abschnitt "MapiSvc. inf [Services]"</span><span class="sxs-lookup"><span data-stu-id="e03ac-103">MapiSvc.inf [Services] Section</span></span>

  
  
<span data-ttu-id="e03ac-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e03ac-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e03ac-105">Im Abschnitt **[Dienste]** werden die Nachrichtendienste aufgelistet, die auf einem Computer installiert sind.</span><span class="sxs-lookup"><span data-stu-id="e03ac-105">The **[Services]** section lists the message services that are installed on a computer.</span></span> <span data-ttu-id="e03ac-106">Die Einträge in diesem Abschnitt verwenden das folgende Format:</span><span class="sxs-lookup"><span data-stu-id="e03ac-106">Entries in this section use the following format:</span></span> 
  
 <span data-ttu-id="e03ac-107">**Services**</span><span class="sxs-lookup"><span data-stu-id="e03ac-107">**[Services]**</span></span>
  
 <span data-ttu-id="e03ac-108">_Message-Service section Name_ =  _Message Service Name_</span><span class="sxs-lookup"><span data-stu-id="e03ac-108">_message-service section name_ =  _message service name_</span></span>
  
<span data-ttu-id="e03ac-109">Der Abschnitt Name des Message-Service-Abschnitts ist eine vom Nachrichtendienst definierte Zeichenfolge, die diesen Eintrag mit einem entsprechenden Abschnitt für den Dienst an anderer Stelle in MAPISVC. inf verknüpft.</span><span class="sxs-lookup"><span data-stu-id="e03ac-109">The message-service section name is a string defined by the message service that links this entry to a corresponding section for the service elsewhere in mapisvc.inf.</span></span> <span data-ttu-id="e03ac-110">Der Name des Nachrichtendiensts ist der Name des installierten Diensts.</span><span class="sxs-lookup"><span data-stu-id="e03ac-110">The message service name is the name of the installed service.</span></span> <span data-ttu-id="e03ac-111">Der folgende Abschnitt zeigt drei Nachrichtendienste: das Standardadressbuch, mein eigener Dienst und der Nachrichtenspeicher Dienst.</span><span class="sxs-lookup"><span data-stu-id="e03ac-111">The following section shows three message services: the Default Address Book, My Own Service, and the Message Store Service.</span></span> <span data-ttu-id="e03ac-112">Diese Dienste sind fiktiv, nur für Illustrationszwecke.</span><span class="sxs-lookup"><span data-stu-id="e03ac-112">These services are fictional, for illustration purposes only.</span></span> <span data-ttu-id="e03ac-113">Jeder Nachrichtendienst Implementierer würde den entsprechenden Eintrag für seinen Nachrichtendienst in diesem Abschnitt ersetzen.</span><span class="sxs-lookup"><span data-stu-id="e03ac-113">Each message service implementer would substitute the appropriate entry for his or her message service in this section.</span></span>
  
```cpp
[Services]
AB=Default Address Book
MsgService=My Own Service
MS=Message Store Service

```

<span data-ttu-id="e03ac-114">Jeder Eintrag in diesem Abschnitt verfügt über einen entsprechenden Abschnitt, in dem Informationen für den Nachrichtendienst gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="e03ac-114">Each entry in this section has a corresponding section of its own where information for the message service is stored.</span></span> <span data-ttu-id="e03ac-115">Der entsprechende Abschnitt für das Standardadressbuch heißt beispielsweise [AB].</span><span class="sxs-lookup"><span data-stu-id="e03ac-115">For example, the corresponding section for the Default Address Book is called [AB].</span></span>
  

