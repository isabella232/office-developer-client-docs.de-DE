---
title: Implementieren der IClassFactory-Schnittstelle für Formularserver
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 22402261-c0fc-49bd-a222-e31989d6ff30
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: ff8766c6211d9820a2beed1fed871f82089b82fb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566782"
---
# <a name="implementing-the-iclassfactory-interface-for-form-servers"></a><span data-ttu-id="13ea4-103">Implementieren der IClassFactory-Schnittstelle für Formularserver</span><span class="sxs-lookup"><span data-stu-id="13ea4-103">Implementing the IClassFactory Interface for Form Servers</span></span>

  
  
<span data-ttu-id="13ea4-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="13ea4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="13ea4-105">[IClassFactory](http://msdn.microsoft.com/en-us/library/ms694364%28VS.85%29.aspx) ist die OLE-Schnittstelle, die Clientanwendungen zum Erstellen neuer Formularobjekte der Nachrichtenklasse des Formulars Servers verwenden.</span><span class="sxs-lookup"><span data-stu-id="13ea4-105">[IClassFactory](http://msdn.microsoft.com/en-us/library/ms694364%28VS.85%29.aspx) is the OLE interface that client applications use to create new form objects of your form server's message class.</span></span> <span data-ttu-id="13ea4-106">Die folgende Tabelle enthält die **IClassFactory** -Methoden, die erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="13ea4-106">The following table lists the **IClassFactory** methods that are required.</span></span> 
  
|<span data-ttu-id="13ea4-107">**Methode**</span><span class="sxs-lookup"><span data-stu-id="13ea4-107">**Method**</span></span>|<span data-ttu-id="13ea4-108">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="13ea4-108">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="13ea4-109">CreateInstance</span><span class="sxs-lookup"><span data-stu-id="13ea4-109">CreateInstance</span></span>](http://msdn.microsoft.com/en-us/library/ms682215%28v=VS.85%29.aspx) <br/> |<span data-ttu-id="13ea4-110">Erstellt ein neues Formularobjekt.</span><span class="sxs-lookup"><span data-stu-id="13ea4-110">Creates a new form object.</span></span>  <br/> |
|[<span data-ttu-id="13ea4-111">LockServer</span><span class="sxs-lookup"><span data-stu-id="13ea4-111">LockServer</span></span>](http://msdn.microsoft.com/en-us/library/ms682332%28v=VS.85%29.aspx) <br/> |<span data-ttu-id="13ea4-112">Sperrt den Formular-Server im Arbeitsspeicher an, sodass Startup Aufwand vermieden werden kann, wenn mehrere Formularobjekte erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="13ea4-112">Locks the form server in memory so that startup overhead can be avoided when multiple form objects are created.</span></span>  <br/> |
   
<span data-ttu-id="13ea4-113">Für alle erforderlichen Informationen zum Implementieren dieser Methods finden Sie unter den Abschnitt COM und ActiveX-Objekt Services im Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="13ea4-113">For all the information necessary to implement these methods, see the COM and ActiveX Object Services section in the Windows SDK.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="13ea4-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="13ea4-114">See also</span></span>



[<span data-ttu-id="13ea4-115">Schreiben von Formularservercode</span><span class="sxs-lookup"><span data-stu-id="13ea4-115">Writing Form Server Code</span></span>](writing-form-server-code.md)

