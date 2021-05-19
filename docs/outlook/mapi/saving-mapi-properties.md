---
title: Speichern von MAPI-Eigenschaften
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ed0c14f9-3dcf-49ad-928e-ba872d4d6b5a
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 5d4653492028151d7e19a5d5490c8c8949002a4f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425890"
---
# <a name="saving-mapi-properties"></a><span data-ttu-id="95bdc-103">Speichern von MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="95bdc-103">Saving MAPI Properties</span></span>

  
  
<span data-ttu-id="95bdc-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="95bdc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="95bdc-105">Viele Objekte unterstützen ein Transaktionsmodell der Verarbeitung, bei dem Änderungen an Eigenschaften erst dann dauerhaft vorgenommen werden, wenn sie zu einem späteren Zeitpunkt ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="95bdc-105">Many objects support a transaction model of processing whereby changes to properties are not made permanent until they are committed at a later time.</span></span> <span data-ttu-id="95bdc-106">Während Änderungen an Eigenschaften von den [Methoden IMAPIProp::SetProps](imapiprop-setprops.md) und [IMAPIProp::D eleteProps](imapiprop-deleteprops.md) behandelt werden, wird der Commitschritt von [IMAPIProp::SaveChanges](imapiprop-savechanges.md)verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="95bdc-106">Whereas changes to properties are handled by the [IMAPIProp::SetProps](imapiprop-setprops.md) and [IMAPIProp::DeleteProps](imapiprop-deleteprops.md) methods, the commit step is handled by [IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span></span> <span data-ttu-id="95bdc-107">Erst nach einem erfolgreichen Aufruf von **SaveChanges** kann auf die neueste Version der Eigenschaften eines Objekts zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="95bdc-107">It isn't until after a successful call to **SaveChanges** that the most recent version of an object's properties can be accessed.</span></span> 
  
<span data-ttu-id="95bdc-108">Wenn **SaveChanges** den Fehlerwert MAPI_E_OBJECT_CHANGED, ist dies eine Warnung, dass ein anderer Client gleichzeitig Änderungen am Objekt übergibt.</span><span class="sxs-lookup"><span data-stu-id="95bdc-108">When **SaveChanges** returns the error value MAPI_E_OBJECT_CHANGED, this is a warning that another client is simultaneously committing changes to the object.</span></span> <span data-ttu-id="95bdc-109">Je nach Anbieter, der das Objekt implementieren kann, können mehrere Clients ein Objekt erfolgreich öffnen, indem sie die **OpenEntry-Methode** mit dem MAPI_MODIFY-Flag-Set aufrufen und ihnen Lese-/Schreibzugriff geben.</span><span class="sxs-lookup"><span data-stu-id="95bdc-109">It is possible, depending on the provider implementing the object, for multiple clients to successfully open an object by calling its **OpenEntry** method with the MAPI_MODIFY flag set, giving them read/write access.</span></span> <span data-ttu-id="95bdc-110">Das Objekt, das von einem solchen **OpenEntry-Aufruf** zurückgegeben wird, ist eine Momentaufnahme der Speicherdaten.</span><span class="sxs-lookup"><span data-stu-id="95bdc-110">The object that is returned from such an **OpenEntry** call is a snapshot of the storage data.</span></span> <span data-ttu-id="95bdc-111">Jeder nachfolgende Versuch, diese Daten zu ändern, kann den vorherigen Versuch überschreiben.</span><span class="sxs-lookup"><span data-stu-id="95bdc-111">Each subsequent attempt to change this data can overwrite the previous attempt.</span></span> 
  
<span data-ttu-id="95bdc-112">Nach dem MAPI_E_OBJECT_CHANGED **von SaveChanges** hat ein Client die Möglichkeit,</span><span class="sxs-lookup"><span data-stu-id="95bdc-112">Upon receiving MAPI_E_OBJECT_CHANGED from **SaveChanges**, a client has the option to:</span></span> 
  
- <span data-ttu-id="95bdc-113">Erstellen Sie eine Kopie des Objekts, um die Änderungen zu speichern.</span><span class="sxs-lookup"><span data-stu-id="95bdc-113">Make a copy of the object to hold the changes.</span></span>
    
- <span data-ttu-id="95bdc-114">Rufen Sie **SaveChanges erneut auf,** und geben Sie FORCE_SAVE.</span><span class="sxs-lookup"><span data-stu-id="95bdc-114">Make another call to **SaveChanges**, specifying FORCE_SAVE.</span></span> 
    
<span data-ttu-id="95bdc-115">Durch das Aufrufen von **SaveChanges** mit FORCE_SAVE-Flag wird das vorherige Speichern überschrieben, und die Änderungen eines Clients werden dauerhaft.</span><span class="sxs-lookup"><span data-stu-id="95bdc-115">Calling **SaveChanges** with the FORCE_SAVE flag overwrites the previous save and makes a client's changes permanent.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="95bdc-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="95bdc-116">See also</span></span>



[<span data-ttu-id="95bdc-117">Übersicht über die MAPI-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="95bdc-117">MAPI Property Overview</span></span>](mapi-property-overview.md)

