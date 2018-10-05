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
ms.openlocfilehash: 12d854b72632653d9e1081c9e726c0fe7087bc27
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25388049"
---
# <a name="implementing-the-iclassfactory-interface-for-form-servers"></a><span data-ttu-id="f46d8-103">Implementieren der IClassFactory-Schnittstelle für Formularserver</span><span class="sxs-lookup"><span data-stu-id="f46d8-103">Implementing the IClassFactory Interface for Form Servers</span></span>

  
  
<span data-ttu-id="f46d8-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f46d8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f46d8-105">[IClassFactory](https://msdn.microsoft.com/library/ms694364%28VS.85%29.aspx) ist die OLE-Schnittstelle, die Clientanwendungen zum Erstellen neuer Formularobjekte der Nachrichtenklasse des Formulars Servers verwenden.</span><span class="sxs-lookup"><span data-stu-id="f46d8-105">[IClassFactory](https://msdn.microsoft.com/library/ms694364%28VS.85%29.aspx) is the OLE interface that client applications use to create new form objects of your form server's message class.</span></span> <span data-ttu-id="f46d8-106">Die folgende Tabelle enthält die **IClassFactory** -Methoden, die erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="f46d8-106">The following table lists the **IClassFactory** methods that are required.</span></span> 
  
|<span data-ttu-id="f46d8-107">**Methode**</span><span class="sxs-lookup"><span data-stu-id="f46d8-107">**Method**</span></span>|<span data-ttu-id="f46d8-108">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f46d8-108">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f46d8-109">CreateInstance</span><span class="sxs-lookup"><span data-stu-id="f46d8-109">CreateInstance</span></span>](https://msdn.microsoft.com/library/ms682215%28v=VS.85%29.aspx) <br/> |<span data-ttu-id="f46d8-110">Erstellt ein neues Formularobjekt.</span><span class="sxs-lookup"><span data-stu-id="f46d8-110">Creates a new form object.</span></span>  <br/> |
|[<span data-ttu-id="f46d8-111">LockServer</span><span class="sxs-lookup"><span data-stu-id="f46d8-111">LockServer</span></span>](https://msdn.microsoft.com/library/ms682332%28v=VS.85%29.aspx) <br/> |<span data-ttu-id="f46d8-112">Sperrt den Formular-Server im Arbeitsspeicher an, sodass Startup Aufwand vermieden werden kann, wenn mehrere Formularobjekte erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="f46d8-112">Locks the form server in memory so that startup overhead can be avoided when multiple form objects are created.</span></span>  <br/> |
   
<span data-ttu-id="f46d8-113">Für alle erforderlichen Informationen zum Implementieren dieser Methods finden Sie unter den Abschnitt COM und ActiveX-Objekt Services im Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="f46d8-113">For all the information necessary to implement these methods, see the COM and ActiveX Object Services section in the Windows SDK.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f46d8-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f46d8-114">See also</span></span>



[<span data-ttu-id="f46d8-115">Schreiben von Formularservercode</span><span class="sxs-lookup"><span data-stu-id="f46d8-115">Writing Form Server Code</span></span>](writing-form-server-code.md)

