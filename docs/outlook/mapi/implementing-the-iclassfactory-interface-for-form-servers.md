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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310031"
---
# <a name="implementing-the-iclassfactory-interface-for-form-servers"></a><span data-ttu-id="8d211-103">Implementieren der IClassFactory-Schnittstelle für Formularserver</span><span class="sxs-lookup"><span data-stu-id="8d211-103">Implementing the IClassFactory Interface for Form Servers</span></span>

  
  
<span data-ttu-id="8d211-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8d211-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8d211-105">[IClassFactory](https://msdn.microsoft.com/library/ms694364%28VS.85%29.aspx) ist die OLE-Schnittstelle, mit der Clientanwendungen neue Formularobjekte der Nachrichtenklasse Ihres Formular Servers erstellen.</span><span class="sxs-lookup"><span data-stu-id="8d211-105">[IClassFactory](https://msdn.microsoft.com/library/ms694364%28VS.85%29.aspx) is the OLE interface that client applications use to create new form objects of your form server's message class.</span></span> <span data-ttu-id="8d211-106">In der folgenden Tabelle sind die **IClassFactory** -Methoden aufgeführt, die erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="8d211-106">The following table lists the **IClassFactory** methods that are required.</span></span> 
  
|<span data-ttu-id="8d211-107">**Methode**</span><span class="sxs-lookup"><span data-stu-id="8d211-107">**Method**</span></span>|<span data-ttu-id="8d211-108">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8d211-108">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8d211-109">CreateInstance</span><span class="sxs-lookup"><span data-stu-id="8d211-109">CreateInstance</span></span>](https://msdn.microsoft.com/library/ms682215%28v=VS.85%29.aspx) <br/> |<span data-ttu-id="8d211-110">Erstellt ein neues Form-Objekt.</span><span class="sxs-lookup"><span data-stu-id="8d211-110">Creates a new form object.</span></span>  <br/> |
|[<span data-ttu-id="8d211-111">LockServer</span><span class="sxs-lookup"><span data-stu-id="8d211-111">LockServer</span></span>](https://msdn.microsoft.com/library/ms682332%28v=VS.85%29.aspx) <br/> |<span data-ttu-id="8d211-112">Sperrt den Formularserver im Arbeitsspeicher, sodass der Start Aufwand vermieden werden kann, wenn mehrere Form-Objekte erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="8d211-112">Locks the form server in memory so that startup overhead can be avoided when multiple form objects are created.</span></span>  <br/> |
   
<span data-ttu-id="8d211-113">Alle Informationen, die für die Implementierung dieser Methoden erforderlich sind, finden Sie im Abschnitt com-und ActiveX-Objektdienste im Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="8d211-113">For all the information necessary to implement these methods, see the COM and ActiveX Object Services section in the Windows SDK.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8d211-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8d211-114">See also</span></span>



[<span data-ttu-id="8d211-115">Schreiben von Formular Server Code</span><span class="sxs-lookup"><span data-stu-id="8d211-115">Writing Form Server Code</span></span>](writing-form-server-code.md)

