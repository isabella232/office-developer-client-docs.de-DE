---
title: Abschnitt MapiSvc.inf [Services]
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 99f8e623-3138-4def-9778-5580326111a5
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 19031f6c02f3e8e925adfc8d2affa43fb6532fee
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793154"
---
# <a name="mapisvcinf-services-section"></a><span data-ttu-id="11b35-103">Abschnitt MapiSvc.inf [Services]</span><span class="sxs-lookup"><span data-stu-id="11b35-103">MapiSvc.inf [Services] Section</span></span>

  
  
<span data-ttu-id="11b35-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="11b35-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="11b35-105">Im Abschnitt **[Services]** werden die Nachrichtendienste, die auf einem Computer installiert sind.</span><span class="sxs-lookup"><span data-stu-id="11b35-105">The **[Services]** section lists the message services that are installed on a computer.</span></span> <span data-ttu-id="11b35-106">Einträge in diesem Abschnitt verwenden Sie das folgende Format:</span><span class="sxs-lookup"><span data-stu-id="11b35-106">Entries in this section use the following format:</span></span> 
  
 <span data-ttu-id="11b35-107">**[Services]**</span><span class="sxs-lookup"><span data-stu-id="11b35-107">**[Services]**</span></span>
  
 <span data-ttu-id="11b35-108">_Message-Dienst im Abschnittsname_ =  _Dienstname Nachricht_</span><span class="sxs-lookup"><span data-stu-id="11b35-108">_message-service section name_ =  _message service name_</span></span>
  
<span data-ttu-id="11b35-109">Den Namen des Abschnitts Message-Dienst ist eine Zeichenfolge vom Nachrichtendienst enthält, die dieser Eintrag einen entsprechenden Abschnitt für den Dienst an anderer Stelle im mapisvc.inf definiert.</span><span class="sxs-lookup"><span data-stu-id="11b35-109">The message-service section name is a string defined by the message service that links this entry to a corresponding section for the service elsewhere in mapisvc.inf.</span></span> <span data-ttu-id="11b35-110">Der Dienstname Nachricht ist der Name des installierten Dienstes.</span><span class="sxs-lookup"><span data-stu-id="11b35-110">The message service name is the name of the installed service.</span></span> <span data-ttu-id="11b35-111">Der folgende Abschnitt zeigt drei Message-Dienste: das Standard-Adressbuch, meine eigenen Service und den Informationsspeicher-Dienst.</span><span class="sxs-lookup"><span data-stu-id="11b35-111">The following section shows three message services: the Default Address Book, My Own Service, and the Message Store Service.</span></span> <span data-ttu-id="11b35-112">Diese Dienste sind nur zur Veranschaulichung fiktiv.</span><span class="sxs-lookup"><span data-stu-id="11b35-112">These services are fictional, for illustration purposes only.</span></span> <span data-ttu-id="11b35-113">Jede Nachricht Service Implementierer würde durch den entsprechenden Eintrag für seine Messagingdiensts in diesem Abschnitt ersetzen.</span><span class="sxs-lookup"><span data-stu-id="11b35-113">Each message service implementer would substitute the appropriate entry for his or her message service in this section.</span></span>
  
```cpp
[Services]
AB=Default Address Book
MsgService=My Own Service
MS=Message Store Service

```

<span data-ttu-id="11b35-114">Jeder Eintrag in diesem Abschnitt hat einen entsprechenden Abschnitt eigene, in dem Informationen für den Dienst gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="11b35-114">Each entry in this section has a corresponding section of its own where information for the message service is stored.</span></span> <span data-ttu-id="11b35-115">Beispielsweise wird im entsprechende Abschnitt für das Standard-Adressbuch [AB] aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="11b35-115">For example, the corresponding section for the Default Address Book is called [AB].</span></span>
  

