---
title: MAPI-fortSchrittsIndikatoren
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 73a99e52-97fe-40f5-af90-52cfd858ab22
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: cdfb6898146583b7da9b043eadd3acc09edbf292
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328210"
---
# <a name="mapi-progress-indicators"></a><span data-ttu-id="6e82d-103">MAPI-fortSchrittsIndikatoren</span><span class="sxs-lookup"><span data-stu-id="6e82d-103">MAPI Progress Indicators</span></span>

  
  
<span data-ttu-id="6e82d-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6e82d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6e82d-105">Viele der Vorgänge, die Sie für Clients ausführen, können sehr viel Zeit in Anspruch nehmen.</span><span class="sxs-lookup"><span data-stu-id="6e82d-105">Many of the operations that you perform for clients can take a long time to complete.</span></span> <span data-ttu-id="6e82d-106">Wenn Sie Clients über den Fortschritt eines längeren Vorgangs informieren möchten, können Sie einen Indikator anzeigen, der den abgeschlossenen Teil eines Vorgangs zu einem beliebigen Zeitpunkt vom Beginn des Vorgangs bis zum Abschluss grafisch anzeigt.</span><span class="sxs-lookup"><span data-stu-id="6e82d-106">To inform clients of the progress of a lengthy operation, you can show an indicator that displays graphically the finished portion of an operation at any given point from the start of the operation to its completion.</span></span> <span data-ttu-id="6e82d-107">Die Fortschrittsanzeige zeigt einen Prozentsatz der gesamten auszufüllenden Operation an.</span><span class="sxs-lookup"><span data-stu-id="6e82d-107">The progress indicator shows a percentage of the total operation to be completed.</span></span>
  
<span data-ttu-id="6e82d-108">Die folgenden Methoden unterstützen langwierige Vorgänge und die Anzeige einer Statusanzeige:</span><span class="sxs-lookup"><span data-stu-id="6e82d-108">The following methods support lengthy operations and the display of a progress indicator:</span></span>
  
- <span data-ttu-id="6e82d-109">[IMAPIFolder:: CopyMessages](imapifolder-copymessages.md), [IMAPIFolder:: CopyFolder](imapifolder-copyfolder.md), [IMAPIFolder::D Eletemessages](imapifolder-deletemessages.md), [IMAPIFolder::D Eletefolder](imapifolder-deletefolder.md), [IMAPIFolder:: EmptyFolder](imapifolder-emptyfolder.md)und [IMAPIFolder:: SetReadFlags](imapifolder-setreadflags.md).</span><span class="sxs-lookup"><span data-stu-id="6e82d-109">[IMAPIFolder::CopyMessages](imapifolder-copymessages.md), [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md), [IMAPIFolder::DeleteMessages](imapifolder-deletemessages.md), [IMAPIFolder::DeleteFolder](imapifolder-deletefolder.md), [IMAPIFolder::EmptyFolder](imapifolder-emptyfolder.md), and [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md).</span></span>
    
- <span data-ttu-id="6e82d-110">[IMAPIProp:: CopyProps](imapiprop-copyprops.md) und [IMAPIProp:: CopyTo](imapiprop-copyto.md).</span><span class="sxs-lookup"><span data-stu-id="6e82d-110">[IMAPIProp::CopyProps](imapiprop-copyprops.md) and [IMAPIProp::CopyTo](imapiprop-copyto.md).</span></span>
    
- <span data-ttu-id="6e82d-111">[IMAPISupport::D ocopyprops](imapisupport-docopyprops.md), [IMAPISupport::D ocopyto](imapisupport-docopyto.md), [IMAPISupport:: CopyFolder](imapisupport-copyfolder.md)und [IMAPISupport:: CopyMessages](imapisupport-copymessages.md).</span><span class="sxs-lookup"><span data-stu-id="6e82d-111">[IMAPISupport::DoCopyProps](imapisupport-docopyprops.md), [IMAPISupport::DoCopyTo](imapisupport-docopyto.md), [IMAPISupport::CopyFolder](imapisupport-copyfolder.md), and [IMAPISupport::CopyMessages](imapisupport-copymessages.md).</span></span>
    
- <span data-ttu-id="6e82d-112">[IMessage::D eleteattach](imessage-deleteattach.md).</span><span class="sxs-lookup"><span data-stu-id="6e82d-112">[IMessage::DeleteAttach](imessage-deleteattach.md).</span></span>
    
- <span data-ttu-id="6e82d-113">[IABContainer:: CopyEntries](iabcontainer-copyentries.md).</span><span class="sxs-lookup"><span data-stu-id="6e82d-113">[IABContainer::CopyEntries](iabcontainer-copyentries.md).</span></span>
    
<span data-ttu-id="6e82d-114">Um eine Statusanzeige anzuzeigen, definiert MAPI ein Progress-Objekt.</span><span class="sxs-lookup"><span data-stu-id="6e82d-114">To display a progress indicator, MAPI defines a progress object.</span></span> <span data-ttu-id="6e82d-115">Progress-Objekte implementieren die [IMAPIProgress: IUnknown](imapiprogressiunknown.md) -Schnittstelle, eine Schnittstelle, die Methoden zum Festlegen des Indikators und zum Erstellen der Anzeige enthält.</span><span class="sxs-lookup"><span data-stu-id="6e82d-115">Progress objects implement the [IMAPIProgress : IUnknown](imapiprogressiunknown.md) interface, an interface that includes methods for establishing the range of the indicator and creating the display.</span></span> <span data-ttu-id="6e82d-116">MAPI bietet eine Progress-Objekt Implementierung wie einige Clients.</span><span class="sxs-lookup"><span data-stu-id="6e82d-116">MAPI provides a progress object implementation as do some clients.</span></span> <span data-ttu-id="6e82d-117">Sie sollten die Implementierung eines Clients, sofern vorhanden, als Eingabeparameter für die Methode verwenden, die den Vorgang ausführt.</span><span class="sxs-lookup"><span data-stu-id="6e82d-117">You should use a client's implementation, if one is supplied, as an input parameter to the method performing the operation.</span></span> <span data-ttu-id="6e82d-118">Wenn der Client NULL anstelle eines Zeigers an ein Progress-Objekt übergibt, verwenden Sie die MAPI-Implementierung, indem Sie die [IMAPISupport::D oprogressdialog](imapisupport-doprogressdialog.md) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="6e82d-118">If the client passes NULL instead of a pointer to a progress object, use MAPI's implementation by calling the [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6e82d-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6e82d-119">See also</span></span>



[<span data-ttu-id="6e82d-120">MAPI-Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="6e82d-120">MAPI Service Providers</span></span>](mapi-service-providers.md)

