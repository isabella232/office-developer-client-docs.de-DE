---
title: MAPI-Statusanzeigen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 73a99e52-97fe-40f5-af90-52cfd858ab22
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: d8af2ba3067dabe759056313eb278b9901510980
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793043"
---
# <a name="mapi-progress-indicators"></a><span data-ttu-id="70d1d-103">MAPI-Statusanzeigen</span><span class="sxs-lookup"><span data-stu-id="70d1d-103">MAPI Progress Indicators</span></span>

  
  
<span data-ttu-id="70d1d-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="70d1d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="70d1d-105">Viele Vorgänge, die Sie für Clients ausführen dauert sehr lange Zeit in Anspruch.</span><span class="sxs-lookup"><span data-stu-id="70d1d-105">Many of the operations that you perform for clients can take a long time to complete.</span></span> <span data-ttu-id="70d1d-106">Um den Fortschritt eines längeren Vorgangs-Clients zu informieren, können Sie ein Symbol anzeigen, das den Teil eines Vorgangs nach Abschluss des Vorgangs zu einem bestimmten Zeitpunkt vom Anfang des Vorgangs zu ihrem Abschluss grafisch dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="70d1d-106">To inform clients of the progress of a lengthy operation, you can show an indicator that displays graphically the finished portion of an operation at any given point from the start of the operation to its completion.</span></span> <span data-ttu-id="70d1d-107">Die Statusanzeige zeigt einen prozentualen Anteil der gesamte Vorgang ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="70d1d-107">The progress indicator shows a percentage of the total operation to be completed.</span></span>
  
<span data-ttu-id="70d1d-108">Die folgenden Methoden unterstützen langen Vorgänge und die Anzeige einer Statusanzeige:</span><span class="sxs-lookup"><span data-stu-id="70d1d-108">The following methods support lengthy operations and the display of a progress indicator:</span></span>
  
- <span data-ttu-id="70d1d-109">[IMAPIFolder::CopyMessages](imapifolder-copymessages.md), [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md), [IMAPIFolder::DeleteMessages](imapifolder-deletemessages.md), [IMAPIFolder::DeleteFolder](imapifolder-deletefolder.md), [IMAPIFolder::EmptyFolder](imapifolder-emptyfolder.md)und [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md).</span><span class="sxs-lookup"><span data-stu-id="70d1d-109">[IMAPIFolder::CopyMessages](imapifolder-copymessages.md), [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md), [IMAPIFolder::DeleteMessages](imapifolder-deletemessages.md), [IMAPIFolder::DeleteFolder](imapifolder-deletefolder.md), [IMAPIFolder::EmptyFolder](imapifolder-emptyfolder.md), and [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md).</span></span>
    
- <span data-ttu-id="70d1d-110">[IMAPIProp::CopyProps](imapiprop-copyprops.md) und [IMAPIProp::CopyTo](imapiprop-copyto.md).</span><span class="sxs-lookup"><span data-stu-id="70d1d-110">[IMAPIProp::CopyProps](imapiprop-copyprops.md) and [IMAPIProp::CopyTo](imapiprop-copyto.md).</span></span>
    
- <span data-ttu-id="70d1d-111">[IMAPISupport::DoCopyProps](imapisupport-docopyprops.md), [IMAPISupport::DoCopyTo](imapisupport-docopyto.md), [IMAPISupport::CopyFolder](imapisupport-copyfolder.md)und [IMAPISupport::CopyMessages](imapisupport-copymessages.md).</span><span class="sxs-lookup"><span data-stu-id="70d1d-111">[IMAPISupport::DoCopyProps](imapisupport-docopyprops.md), [IMAPISupport::DoCopyTo](imapisupport-docopyto.md), [IMAPISupport::CopyFolder](imapisupport-copyfolder.md), and [IMAPISupport::CopyMessages](imapisupport-copymessages.md).</span></span>
    
- <span data-ttu-id="70d1d-112">[IMessage::DeleteAttach](imessage-deleteattach.md).</span><span class="sxs-lookup"><span data-stu-id="70d1d-112">[IMessage::DeleteAttach](imessage-deleteattach.md).</span></span>
    
- <span data-ttu-id="70d1d-113">[IABContainer::CopyEntries](iabcontainer-copyentries.md).</span><span class="sxs-lookup"><span data-stu-id="70d1d-113">[IABContainer::CopyEntries](iabcontainer-copyentries.md).</span></span>
    
<span data-ttu-id="70d1d-114">Zum Anzeigen einer Statusanzeige definiert MAPI ein Fortschritt-Objekt.</span><span class="sxs-lookup"><span data-stu-id="70d1d-114">To display a progress indicator, MAPI defines a progress object.</span></span> <span data-ttu-id="70d1d-115">Fortschritt Objekte Implementieren der [IMAPIProgress: IUnknown](imapiprogressiunknown.md) -Schnittstelle, die eine Schnittstelle, die Methoden für das Einrichten des Bereichs von den Indikator und die Anzeige erstellen enthält.</span><span class="sxs-lookup"><span data-stu-id="70d1d-115">Progress objects implement the [IMAPIProgress : IUnknown](imapiprogressiunknown.md) interface, an interface that includes methods for establishing the range of the indicator and creating the display.</span></span> <span data-ttu-id="70d1d-116">MAPI bietet eine Implementierung der Fortschritt-Objekt, wie einige Clients.</span><span class="sxs-lookup"><span data-stu-id="70d1d-116">MAPI provides a progress object implementation as do some clients.</span></span> <span data-ttu-id="70d1d-117">Sie sollten eine Client-Implementierung verwenden, wenn eine bereitgestellt wird, als Eingabeparameter der Methode Ausführen des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="70d1d-117">You should use a client's implementation, if one is supplied, as an input parameter to the method performing the operation.</span></span> <span data-ttu-id="70d1d-118">Wenn der Client NULL anstatt einen Zeiger auf ein Objekt Fortschritt übergibt, verwenden Sie des MAPI-Implementierung durch Aufrufen der [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="70d1d-118">If the client passes NULL instead of a pointer to a progress object, use MAPI's implementation by calling the [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="70d1d-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="70d1d-119">See also</span></span>



[<span data-ttu-id="70d1d-120">MAPI-Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="70d1d-120">MAPI Service Providers</span></span>](mapi-service-providers.md)

