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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283086"
---
# <a name="saving-mapi-properties"></a><span data-ttu-id="9f6c8-103">Speichern von MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9f6c8-103">Saving MAPI Properties</span></span>

  
  
<span data-ttu-id="9f6c8-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9f6c8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9f6c8-105">Viele Objekte unterstützen ein Transaktionsmodell der Verarbeitung, wodurch Änderungen an Eigenschaften nicht dauerhaft vorgenommen werden, bis Sie zu einem späteren Zeitpunkt ein Commit ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="9f6c8-105">Many objects support a transaction model of processing whereby changes to properties are not made permanent until they are committed at a later time.</span></span> <span data-ttu-id="9f6c8-106">Während Änderungen an Eigenschaften von den [IMAPIProp::](imapiprop-setprops.md) SetProps-und [IMAPIProp::D-eleteprops](imapiprop-deleteprops.md) -Methoden verarbeitet werden, wird der Commit-Schritt von [IMAPIProp:: SaveChanges](imapiprop-savechanges.md)verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="9f6c8-106">Whereas changes to properties are handled by the [IMAPIProp::SetProps](imapiprop-setprops.md) and [IMAPIProp::DeleteProps](imapiprop-deleteprops.md) methods, the commit step is handled by [IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span></span> <span data-ttu-id="9f6c8-107">Erst nach einem erfolgreichen Aufruf von SaveChanges \*\*\*\* kann auf die neueste Version der Eigenschaften eines Objekts zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="9f6c8-107">It isn't until after a successful call to **SaveChanges** that the most recent version of an object's properties can be accessed.</span></span> 
  
<span data-ttu-id="9f6c8-108">Wenn **SaveChanges** den Fehlerwert MAPI_E_OBJECT_CHANGED zurückgibt, ist dies eine Warnung, dass ein anderer Client gleichzeitig Änderungen an dem Objekt ausführt.</span><span class="sxs-lookup"><span data-stu-id="9f6c8-108">When **SaveChanges** returns the error value MAPI_E_OBJECT_CHANGED, this is a warning that another client is simultaneously committing changes to the object.</span></span> <span data-ttu-id="9f6c8-109">Abhängig vom Anbieter, der das Objekt implementiert, ist es möglich, dass mehrere Clients ein Objekt erfolgreich öffnen, indem Sie die **OpenEntry** -Methode mit dem MAPI_MODIFY-Flag-Satz aufrufen, um Ihnen Lese-/Schreibzugriff zu erteilen.</span><span class="sxs-lookup"><span data-stu-id="9f6c8-109">It is possible, depending on the provider implementing the object, for multiple clients to successfully open an object by calling its **OpenEntry** method with the MAPI_MODIFY flag set, giving them read/write access.</span></span> <span data-ttu-id="9f6c8-110">Das Objekt, das von einem solchen **OpenEntry** -Aufruf zurückgegeben wird, ist eine Momentaufnahme der Speicherdaten.</span><span class="sxs-lookup"><span data-stu-id="9f6c8-110">The object that is returned from such an **OpenEntry** call is a snapshot of the storage data.</span></span> <span data-ttu-id="9f6c8-111">Jeder nachfolgende Versuch, diese Daten zu ändern, kann den vorherigen Versuch überschreiben.</span><span class="sxs-lookup"><span data-stu-id="9f6c8-111">Each subsequent attempt to change this data can overwrite the previous attempt.</span></span> 
  
<span data-ttu-id="9f6c8-112">Wenn Sie MAPI_E_OBJECT_CHANGED von **SaveChanges**empfangen, hat der Client folgende Möglichkeiten:</span><span class="sxs-lookup"><span data-stu-id="9f6c8-112">Upon receiving MAPI_E_OBJECT_CHANGED from **SaveChanges**, a client has the option to:</span></span> 
  
- <span data-ttu-id="9f6c8-113">Erstellen Sie eine Kopie des Objekts, um die Änderungen zu speichern.</span><span class="sxs-lookup"><span data-stu-id="9f6c8-113">Make a copy of the object to hold the changes.</span></span>
    
- <span data-ttu-id="9f6c8-114">Führen Sie einen weiteren \*\*\*\* Aufruf von SaveChanges aus, und geben Sie FORCE_SAVE.</span><span class="sxs-lookup"><span data-stu-id="9f6c8-114">Make another call to **SaveChanges**, specifying FORCE_SAVE.</span></span> 
    
<span data-ttu-id="9f6c8-115">Das \*\*\*\* Aufrufen von SaveChanges mit dem FORCE_SAVE-Flag überschreibt den vorherigen Speicher und macht die Änderungen eines Clients dauerhaft.</span><span class="sxs-lookup"><span data-stu-id="9f6c8-115">Calling **SaveChanges** with the FORCE_SAVE flag overwrites the previous save and makes a client's changes permanent.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9f6c8-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9f6c8-116">See also</span></span>



[<span data-ttu-id="9f6c8-117">Übersicht über die MAPI-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="9f6c8-117">MAPI Property Overview</span></span>](mapi-property-overview.md)

