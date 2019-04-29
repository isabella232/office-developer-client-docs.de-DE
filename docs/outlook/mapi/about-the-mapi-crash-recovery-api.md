---
title: Informationen über die API zur MAPI-Wiederherstellung nach einem Absturz
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: bc1e1f55-1959-a4a9-a24d-f006af531c9a
description: 'Letzte �nderung: Montag, 25. Juni 2012'
ms.openlocfilehash: 1acca6d806c1734007ac7c5e41059d3a870dc5bb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420262"
---
# <a name="about-the-mapi-crash-recovery-api"></a><span data-ttu-id="edd86-103">Informationen über die API zur MAPI-Wiederherstellung nach einem Absturz</span><span class="sxs-lookup"><span data-stu-id="edd86-103">About the MAPI Crash Recovery API</span></span>

  
  
<span data-ttu-id="edd86-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="edd86-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="edd86-105">Die MAPI-Notfall wiederHerstellungs-API überprüft den Status des freigegebenen Speichers (PST) oder der Offline Ordner Datei (OST), um sicherzustellen, dass die Daten konsistent sind.</span><span class="sxs-lookup"><span data-stu-id="edd86-105">The MAPI Crash Recovery API checks the state of the Personal Folders file (PST) or Offline Folders file (OST) shared memory to verify that the data is in a consistent state.</span></span> <span data-ttu-id="edd86-106">Wenn Sie sich in einem konsistenten Zustand befindet, verschiebt die [MAPICrashRecovery](mapicrashrecovery.md) -Funktion die Daten aus dem geöffneten PST-oder Kosten auf den Datenträger und sperrt die PST oder Kosten und lässt keinen Lese-oder Schreibzugriff auf die Daten zu.</span><span class="sxs-lookup"><span data-stu-id="edd86-106">If it is in a consistent state, the [MAPICrashRecovery](mapicrashrecovery.md) function moves the data from the open PSTs or OSTs to disk and locks the PSTs or OSTs and does not allow any read or write access to the data.</span></span> <span data-ttu-id="edd86-107">Dadurch wird sichergestellt, dass die Daten in einem konsistenten Zustand bleiben, bis der Prozess beendet wird.</span><span class="sxs-lookup"><span data-stu-id="edd86-107">This ensures that the data remains in a consistent state until the process is terminated.</span></span> <span data-ttu-id="edd86-108">Wenn Sie sicherstellen, dass sich PST oder Kosten in einem konsistenten Zustand befinden, bevor der Prozess beendet wird, können Sie verhindern, dass Microsoft Outlook 2013 und Microsoft Outlook 2010 die folgende Fehlermeldung anzeigen und Leistungsprobleme vermeiden.</span><span class="sxs-lookup"><span data-stu-id="edd86-108">By ensuring that the PSTs or OSTs are in a consistent state before the process is terminated, you can prevent Microsoft Outlook 2013 and Microsoft Outlook 2010 from displaying the following error message and avoid performance problems.</span></span> 
  
 <span data-ttu-id="edd86-109">**Eine Datendatei wurde bei der letzten Verwendung nicht ordnungsgemäß geschlossen und wird auf Probleme überprüft. Die Leistung kann beeinträchtigt werden, während die Überprüfung ausgeführt wird.**</span><span class="sxs-lookup"><span data-stu-id="edd86-109">**A data file did not close properly the last time it was used and is being checked for problems. Performance might be affected while the check is in progress.**</span></span>
  
<span data-ttu-id="edd86-110">Diese API bietet Folgendes:</span><span class="sxs-lookup"><span data-stu-id="edd86-110">This API provides the following:</span></span>
  
<span data-ttu-id="edd86-111">Konstanten</span><span class="sxs-lookup"><span data-stu-id="edd86-111">Constants:</span></span>
  
- [<span data-ttu-id="edd86-112">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="edd86-112">MAPI Constants</span></span>](mapi-constants.md)
    
<span data-ttu-id="edd86-113">Funktionen:</span><span class="sxs-lookup"><span data-stu-id="edd86-113">Functions:</span></span>
  
- [<span data-ttu-id="edd86-114">MAPICrashRecovery</span><span class="sxs-lookup"><span data-stu-id="edd86-114">MAPICrashRecovery</span></span>](mapicrashrecovery.md)
    
## <a name="see-also"></a><span data-ttu-id="edd86-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="edd86-115">See also</span></span>



[<span data-ttu-id="edd86-116">Verwenden der API zur MAPI-Wiederherstellung nach einem Absturz</span><span class="sxs-lookup"><span data-stu-id="edd86-116">Use the MAPI Crash Recovery API</span></span>](how-to-use-the-mapi-crash-recovery-api.md)

