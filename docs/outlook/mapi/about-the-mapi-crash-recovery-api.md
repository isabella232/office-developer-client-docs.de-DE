---
title: Informationen über die API zur MAPI-Wiederherstellung nach einem Absturz
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: bc1e1f55-1959-a4a9-a24d-f006af531c9a
description: 'Letzte �nderung: Montag, 25. Juni 2012'
ms.openlocfilehash: 34589860ed25f8236a343e16679c2e7a6bdd1e2b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791237"
---
# <a name="about-the-mapi-crash-recovery-api"></a><span data-ttu-id="978c6-103">Informationen über die API zur MAPI-Wiederherstellung nach einem Absturz</span><span class="sxs-lookup"><span data-stu-id="978c6-103">About the MAPI Crash Recovery API</span></span>

  
  
<span data-ttu-id="978c6-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="978c6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="978c6-105">MAPI-abstürzen Wiederherstellung API überprüft der Status der Persönliche Ordner-Datei (PST) oder Offlineordnerdatei (OST) freigegebenen Speicher, um sicherzustellen, dass die Daten in einer konsistenten Zustand befindet.</span><span class="sxs-lookup"><span data-stu-id="978c6-105">The MAPI Crash Recovery API checks the state of the Personal Folders file (PST) or Offline Folders file (OST) shared memory to verify that the data is in a consistent state.</span></span> <span data-ttu-id="978c6-106">Ist in einen konsistenten Status, verschiebt die Daten aus dem open PST-Dateien oder OSTs auf dem Datenträger die [MAPICrashRecovery](mapicrashrecovery.md) -Funktion und sperrt die PST-Dateien oder OSTs und lässt keine Lese- oder Schreibzugriff auf die Daten.</span><span class="sxs-lookup"><span data-stu-id="978c6-106">If it is in a consistent state, the [MAPICrashRecovery](mapicrashrecovery.md) function moves the data from the open PSTs or OSTs to disk and locks the PSTs or OSTs and does not allow any read or write access to the data.</span></span> <span data-ttu-id="978c6-107">Dadurch wird sichergestellt, dass die Konsistenz der gelesenen Daten, bis der Prozess beendet wird.</span><span class="sxs-lookup"><span data-stu-id="978c6-107">This ensures that the data remains in a consistent state until the process is terminated.</span></span> <span data-ttu-id="978c6-108">Sicherstellen, dass die PST-Dateien oder OSTs einen konsistenten Status befinden, bevor der Prozess beendet wird, können Sie verhindern, dass Microsoft Outlook 2013 und Microsoft Outlook 2010 die folgende Fehlermeldung angezeigt und Leistungsprobleme vermeiden.</span><span class="sxs-lookup"><span data-stu-id="978c6-108">By ensuring that the PSTs or OSTs are in a consistent state before the process is terminated, you can prevent Microsoft Outlook 2013 and Microsoft Outlook 2010 from displaying the following error message and avoid performance problems.</span></span> 
  
 <span data-ttu-id="978c6-109">**Eine Datei wurde nicht ordnungsgemäß geschlossen zuletzt verwendet wurde, und es wird überprüft für Probleme. Während das Kontrollkästchen ausgeführt wird, kann die Leistung beeinträchtigen.**</span><span class="sxs-lookup"><span data-stu-id="978c6-109">**A data file did not close properly the last time it was used and is being checked for problems. Performance might be affected while the check is in progress.**</span></span>
  
<span data-ttu-id="978c6-110">Diese API bietet folgende Funktionen:</span><span class="sxs-lookup"><span data-stu-id="978c6-110">This API provides the following:</span></span>
  
<span data-ttu-id="978c6-111">Konstanten:</span><span class="sxs-lookup"><span data-stu-id="978c6-111">Constants:</span></span>
  
- [<span data-ttu-id="978c6-112">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="978c6-112">MAPI Constants</span></span>](mapi-constants.md)
    
<span data-ttu-id="978c6-113">Funktionen:</span><span class="sxs-lookup"><span data-stu-id="978c6-113">Functions:</span></span>
  
- [<span data-ttu-id="978c6-114">MAPICrashRecovery</span><span class="sxs-lookup"><span data-stu-id="978c6-114">MAPICrashRecovery</span></span>](mapicrashrecovery.md)
    
## <a name="see-also"></a><span data-ttu-id="978c6-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="978c6-115">See also</span></span>



[<span data-ttu-id="978c6-116">Verwenden der API zur MAPI-Wiederherstellung nach einem Absturz</span><span class="sxs-lookup"><span data-stu-id="978c6-116">Use the MAPI Crash Recovery API</span></span>](how-to-use-the-mapi-crash-recovery-api.md)

