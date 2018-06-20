---
title: Die Einstellungsoptionen für das Adressbuch
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9bd31233-fc8d-4e0a-9f1b-218c5ecb6d1b
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: c64f84da6bece809176bf67985b6f55ce92414a2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795512"
---
# <a name="setting-address-book-options"></a><span data-ttu-id="27b4b-103">Die Einstellungsoptionen für das Adressbuch</span><span class="sxs-lookup"><span data-stu-id="27b4b-103">Setting Address Book Options</span></span>

  
  
<span data-ttu-id="27b4b-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="27b4b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="27b4b-105">Sie können drei Eigenschaften festlegen, die Optionen für die Verwendung des Adressbuchs beschreiben:</span><span class="sxs-lookup"><span data-stu-id="27b4b-105">You can set three properties that describe options for using the address book:</span></span>
  
- <span data-ttu-id="27b4b-106">**PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="27b4b-106">**PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md))</span></span>
    
    <span data-ttu-id="27b4b-107">Die **PR_AB_SEARCH_PATH** -Eigenschaft wird von [IAddrBook::ResolveName](iaddrbook-resolvename.md) zum Bestimmen der Container werden im Zusammenhang mit Auflösung und die Reihenfolge, in der sie zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="27b4b-107">The **PR_AB_SEARCH_PATH** property is used by [IAddrBook::ResolveName](iaddrbook-resolvename.md) to determine the containers to be involved in name resolution and the order that they should be involved.</span></span> <span data-ttu-id="27b4b-108">Für jeden Container in **PR_AB_SEARCH_PATH**ruft **IAddrBook::ResolveName** seine [IABContainer](iabcontainer-resolvenames.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="27b4b-108">For each container in **PR_AB_SEARCH_PATH**, **IAddrBook::ResolveName** calls its [IABContainer::ResolveNames](iabcontainer-resolvenames.md) method.</span></span> <span data-ttu-id="27b4b-109">Container am Anfang des **PR_AB_SEARCH_PATH** sind vor dem Container am Ende des **PR_AB_SEARCH_PATH**durchsucht.</span><span class="sxs-lookup"><span data-stu-id="27b4b-109">Containers at the beginning of **PR_AB_SEARCH_PATH** are searched before containers at the end of **PR_AB_SEARCH_PATH**.</span></span> 
    
    <span data-ttu-id="27b4b-110">Die Reihenfolge der Suche in **PR_AB_SEARCH_PATH** wird angegeben, mithilfe der Struktur einer [SRowSet](srowset.md) , die dieselbe Struktur, die verwendet wird, um die Zeilen in einer Tabelle darstellen.</span><span class="sxs-lookup"><span data-stu-id="27b4b-110">The search order in **PR_AB_SEARCH_PATH** is specified using an [SRowSet](srowset.md) structure, the same structure that is used to represent rows in a table.</span></span> <span data-ttu-id="27b4b-111">Sie können den aktuellen Suchpfad durch Aufrufen der Methode [IAddrBook::GetSearchPath](iaddrbook-getsearchpath.md) anzeigen und ändern, indem Sie die [IAddrBook::SetSearchPath](iaddrbook-setsearchpath.md) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="27b4b-111">You can view the current search path by calling the [IAddrBook::GetSearchPath](iaddrbook-getsearchpath.md) method and change it by calling the [IAddrBook::SetSearchPath](iaddrbook-setsearchpath.md) method.</span></span> 
    
- <span data-ttu-id="27b4b-112">**PR_AB_DEFAULT_DIR** ([PidTagAbDefaultDir](pidtagabdefaultdir-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="27b4b-112">**PR_AB_DEFAULT_DIR** ([PidTagAbDefaultDir](pidtagabdefaultdir-canonical-property.md))</span></span>
    
    <span data-ttu-id="27b4b-113">Die **PR_AB_DEFAULT_DIR** -Eigenschaft ist die Eintrags-ID der Adressbuchcontainer Anfangs angezeigt werden, wenn im Adressbuch angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="27b4b-113">The **PR_AB_DEFAULT_DIR** property is the entry identifier of the address book container to be displayed initially when the address book is displayed.</span></span> <span data-ttu-id="27b4b-114">Die Standardeinstellung Directory bleibt wirksam, bis Sie ihn ändern, indem Sie die [IAddrBook::SetDefaultDir](iaddrbook-setdefaultdir.md) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="27b4b-114">The default directory setting remains in effect until you change it by calling the [IAddrBook::SetDefaultDir](iaddrbook-setdefaultdir.md) method.</span></span> <span data-ttu-id="27b4b-115">Sie können das Standardverzeichnis durch Aufrufen der Methode [IAddrBook::GetDefaultDir](iaddrbook-getdefaultdir.md) anzeigen.</span><span class="sxs-lookup"><span data-stu-id="27b4b-115">You can view the default directory by calling the [IAddrBook::GetDefaultDir](iaddrbook-getdefaultdir.md) method.</span></span> 
    
- <span data-ttu-id="27b4b-116">**PR_AB_DEFAULT_PAB** ([PidTagAbDefaultPab](pidtagabdefaultpab-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="27b4b-116">**PR_AB_DEFAULT_PAB** ([PidTagAbDefaultPab](pidtagabdefaultpab-canonical-property.md))</span></span>
    
<span data-ttu-id="27b4b-117">Diese drei Eigenschaften sind spezielle, da Sie sie über die Standardmethoden **IMAPIProp** bearbeiten können.</span><span class="sxs-lookup"><span data-stu-id="27b4b-117">These three properties are special because you cannot work with them using the standard **IMAPIProp** methods.</span></span> <span data-ttu-id="27b4b-118">Stattdessen müssen Sie **IAddrBook** Methoden verwenden.</span><span class="sxs-lookup"><span data-stu-id="27b4b-118">Instead, you must use **IAddrBook** methods.</span></span> <span data-ttu-id="27b4b-119">Da keine dieser Eigenschaften mit **IMAPIProp::SetProps**geändert werden kann, ist es nicht erforderlich aufrufen, **IMAPIProp::SaveChanges** , damit Änderungen dauerhaft entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="27b4b-119">Because none of these properties can be changed with **IMAPIProp::SetProps**, there is no need to call **IMAPIProp::SaveChanges** to make changes permanent.</span></span> <span data-ttu-id="27b4b-120">Über die Methoden **IAddrBook** vorgenommenen Änderungen werden sofort wirksam.</span><span class="sxs-lookup"><span data-stu-id="27b4b-120">Modifications made through the **IAddrBook** methods take effect immediately.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="27b4b-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="27b4b-121">See also</span></span>



[<span data-ttu-id="27b4b-122">IAddrBook: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="27b4b-122">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)

