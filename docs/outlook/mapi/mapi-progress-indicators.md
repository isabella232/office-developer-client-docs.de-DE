---
title: MAPI-Fortschrittsindikatoren
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 73a99e52-97fe-40f5-af90-52cfd858ab22
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: cdfb6898146583b7da9b043eadd3acc09edbf292
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410707"
---
# <a name="mapi-progress-indicators"></a><span data-ttu-id="2c7f6-103">MAPI-Fortschrittsindikatoren</span><span class="sxs-lookup"><span data-stu-id="2c7f6-103">MAPI Progress Indicators</span></span>

  
  
<span data-ttu-id="2c7f6-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2c7f6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2c7f6-105">Viele der Vorgänge, die Sie für Clients ausführen, können sehr lange dauern.</span><span class="sxs-lookup"><span data-stu-id="2c7f6-105">Many of the operations that you perform for clients can take a long time to complete.</span></span> <span data-ttu-id="2c7f6-106">Um Clients über den Fortschritt eines langwierigen Vorgangs zu informieren, können Sie einen Indikator anzeigen, der den fertigen Teil eines Vorgangs an einem bestimmten Punkt vom Beginn des Vorgangs bis zum Abschluss grafisch anzeigt.</span><span class="sxs-lookup"><span data-stu-id="2c7f6-106">To inform clients of the progress of a lengthy operation, you can show an indicator that displays graphically the finished portion of an operation at any given point from the start of the operation to its completion.</span></span> <span data-ttu-id="2c7f6-107">Der Fortschrittsindikator zeigt einen Prozentsatz des gesamten vorgangs an, der abgeschlossen werden soll.</span><span class="sxs-lookup"><span data-stu-id="2c7f6-107">The progress indicator shows a percentage of the total operation to be completed.</span></span>
  
<span data-ttu-id="2c7f6-108">Die folgenden Methoden unterstützen langwierige Vorgänge und die Anzeige eines Statusindikators:</span><span class="sxs-lookup"><span data-stu-id="2c7f6-108">The following methods support lengthy operations and the display of a progress indicator:</span></span>
  
- <span data-ttu-id="2c7f6-109">[IMAPIFolder::CopyMessages](imapifolder-copymessages.md), [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md), [IMAPIFolder::D eleteMessages](imapifolder-deletemessages.md), [IMAPIFolder::D eleteFolder](imapifolder-deletefolder.md), [IMAPIFolder::EmptyFolder](imapifolder-emptyfolder.md)und [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md).</span><span class="sxs-lookup"><span data-stu-id="2c7f6-109">[IMAPIFolder::CopyMessages](imapifolder-copymessages.md), [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md), [IMAPIFolder::DeleteMessages](imapifolder-deletemessages.md), [IMAPIFolder::DeleteFolder](imapifolder-deletefolder.md), [IMAPIFolder::EmptyFolder](imapifolder-emptyfolder.md), and [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md).</span></span>
    
- <span data-ttu-id="2c7f6-110">[IMAPIProp::CopyProps](imapiprop-copyprops.md) und [IMAPIProp::CopyTo](imapiprop-copyto.md).</span><span class="sxs-lookup"><span data-stu-id="2c7f6-110">[IMAPIProp::CopyProps](imapiprop-copyprops.md) and [IMAPIProp::CopyTo](imapiprop-copyto.md).</span></span>
    
- <span data-ttu-id="2c7f6-111">[IMAPISupport::D oCopyProps](imapisupport-docopyprops.md), [IMAPISupport::D oCopyTo](imapisupport-docopyto.md), [IMAPISupport::CopyFolder](imapisupport-copyfolder.md)und [IMAPISupport::CopyMessages](imapisupport-copymessages.md).</span><span class="sxs-lookup"><span data-stu-id="2c7f6-111">[IMAPISupport::DoCopyProps](imapisupport-docopyprops.md), [IMAPISupport::DoCopyTo](imapisupport-docopyto.md), [IMAPISupport::CopyFolder](imapisupport-copyfolder.md), and [IMAPISupport::CopyMessages](imapisupport-copymessages.md).</span></span>
    
- <span data-ttu-id="2c7f6-112">[IMessage::D eleteAttach](imessage-deleteattach.md).</span><span class="sxs-lookup"><span data-stu-id="2c7f6-112">[IMessage::DeleteAttach](imessage-deleteattach.md).</span></span>
    
- <span data-ttu-id="2c7f6-113">[IABContainer::CopyEntries](iabcontainer-copyentries.md).</span><span class="sxs-lookup"><span data-stu-id="2c7f6-113">[IABContainer::CopyEntries](iabcontainer-copyentries.md).</span></span>
    
<span data-ttu-id="2c7f6-114">Zum Anzeigen eines Statusindikators definiert MAPI ein Statusobjekt.</span><span class="sxs-lookup"><span data-stu-id="2c7f6-114">To display a progress indicator, MAPI defines a progress object.</span></span> <span data-ttu-id="2c7f6-115">Progress-Objekte implementieren die [IMAPIProgress : IUnknown-Schnittstelle,](imapiprogressiunknown.md) eine Schnittstelle, die Methoden zum Festlegen des Indikatorbereichs und zum Erstellen der Anzeige enthält.</span><span class="sxs-lookup"><span data-stu-id="2c7f6-115">Progress objects implement the [IMAPIProgress : IUnknown](imapiprogressiunknown.md) interface, an interface that includes methods for establishing the range of the indicator and creating the display.</span></span> <span data-ttu-id="2c7f6-116">MAPI stellt eine Progress-Objektimplementierung wie einige Clients zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="2c7f6-116">MAPI provides a progress object implementation as do some clients.</span></span> <span data-ttu-id="2c7f6-117">Wenn eine Clientimplementierung angegeben wird, sollten Sie die Implementierung eines Clients als Eingabeparameter für die Methode verwenden, mit der der Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2c7f6-117">You should use a client's implementation, if one is supplied, as an input parameter to the method performing the operation.</span></span> <span data-ttu-id="2c7f6-118">Wenn der Client NULL anstelle eines Zeigers auf ein Progress-Objekt übergibt, verwenden Sie die MAPI-Implementierung, indem Sie die [IMAPISupport::D oProgressDialog-Methode](imapisupport-doprogressdialog.md) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="2c7f6-118">If the client passes NULL instead of a pointer to a progress object, use MAPI's implementation by calling the [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2c7f6-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2c7f6-119">See also</span></span>



[<span data-ttu-id="2c7f6-120">MAPI-Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="2c7f6-120">MAPI Service Providers</span></span>](mapi-service-providers.md)

