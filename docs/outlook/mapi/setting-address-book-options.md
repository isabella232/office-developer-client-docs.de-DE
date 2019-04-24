---
title: Festlegen von Adressbuchoptionen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9bd31233-fc8d-4e0a-9f1b-218c5ecb6d1b
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: f72c916e917543b11089f8f5ef1aa4b9552a1b6a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351408"
---
# <a name="setting-address-book-options"></a><span data-ttu-id="f0bab-103">Festlegen von Adressbuchoptionen</span><span class="sxs-lookup"><span data-stu-id="f0bab-103">Setting Address Book Options</span></span>

  
  
<span data-ttu-id="f0bab-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f0bab-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f0bab-105">Sie können drei Eigenschaften festlegen, die Optionen für die Verwendung des Adressbuchs beschreiben:</span><span class="sxs-lookup"><span data-stu-id="f0bab-105">You can set three properties that describe options for using the address book:</span></span>
  
- <span data-ttu-id="f0bab-106">**PR_AB_SEARCH_PATH** ([Pidtagabsearchpath (](pidtagabsearchpath-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f0bab-106">**PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md))</span></span>
    
    <span data-ttu-id="f0bab-107">Die **PR_AB_SEARCH_PATH** -Eigenschaft wird von [IAddrBook::](iaddrbook-resolvename.md) ResolveName verwendet, um die an der Namensauflösung beteiligten Container und die Reihenfolge zu bestimmen, in der Sie beteiligt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="f0bab-107">The **PR_AB_SEARCH_PATH** property is used by [IAddrBook::ResolveName](iaddrbook-resolvename.md) to determine the containers to be involved in name resolution and the order that they should be involved.</span></span> <span data-ttu-id="f0bab-108">Für jeden Container in **PR_AB_SEARCH_PATH**ruft **IAddrBook::** ResolveName die [IABContainer:: ResolveNames](iabcontainer-resolvenames.md) -Methode auf.</span><span class="sxs-lookup"><span data-stu-id="f0bab-108">For each container in **PR_AB_SEARCH_PATH**, **IAddrBook::ResolveName** calls its [IABContainer::ResolveNames](iabcontainer-resolvenames.md) method.</span></span> <span data-ttu-id="f0bab-109">Container am Anfang von **PR_AB_SEARCH_PATH** werden vor Containern am Ende von **PR_AB_SEARCH_PATH**durchsucht.</span><span class="sxs-lookup"><span data-stu-id="f0bab-109">Containers at the beginning of **PR_AB_SEARCH_PATH** are searched before containers at the end of **PR_AB_SEARCH_PATH**.</span></span> 
    
    <span data-ttu-id="f0bab-110">Die Suchreihenfolge in **PR_AB_SEARCH_PATH** wird mithilfe einer [SRowSet](srowset.md) -Struktur angegeben, der gleichen Struktur, die zum Darstellen von Zeilen in einer Tabelle verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f0bab-110">The search order in **PR_AB_SEARCH_PATH** is specified using an [SRowSet](srowset.md) structure, the same structure that is used to represent rows in a table.</span></span> <span data-ttu-id="f0bab-111">Sie können den aktuellen Suchpfad anzeigen, indem Sie die [IAddrBook:: GetSearchPath](iaddrbook-getsearchpath.md) -Methode aufrufen und Sie durch Aufrufen der [IAddrBook:: SetSearchPath](iaddrbook-setsearchpath.md) -Methode ändern.</span><span class="sxs-lookup"><span data-stu-id="f0bab-111">You can view the current search path by calling the [IAddrBook::GetSearchPath](iaddrbook-getsearchpath.md) method and change it by calling the [IAddrBook::SetSearchPath](iaddrbook-setsearchpath.md) method.</span></span> 
    
- <span data-ttu-id="f0bab-112">**PR_AB_DEFAULT_DIR** ([Pidtagabdefaultdir (](pidtagabdefaultdir-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f0bab-112">**PR_AB_DEFAULT_DIR** ([PidTagAbDefaultDir](pidtagabdefaultdir-canonical-property.md))</span></span>
    
    <span data-ttu-id="f0bab-113">Die **PR_AB_DEFAULT_DIR** -Eigenschaft ist der Eintragsbezeichner des Adressbuch Containers, der beim Anzeigen des Adressbuchs angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f0bab-113">The **PR_AB_DEFAULT_DIR** property is the entry identifier of the address book container to be displayed initially when the address book is displayed.</span></span> <span data-ttu-id="f0bab-114">Die Standardverzeichnis Einstellung bleibt wirksam, bis Sie Sie ändern, indem Sie die [IAddrBook:: SetDefaultDir](iaddrbook-setdefaultdir.md) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="f0bab-114">The default directory setting remains in effect until you change it by calling the [IAddrBook::SetDefaultDir](iaddrbook-setdefaultdir.md) method.</span></span> <span data-ttu-id="f0bab-115">Sie können das Standardverzeichnis anzeigen, indem Sie die [IAddrBook:: GetDefaultDir](iaddrbook-getdefaultdir.md) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="f0bab-115">You can view the default directory by calling the [IAddrBook::GetDefaultDir](iaddrbook-getdefaultdir.md) method.</span></span> 
    
- <span data-ttu-id="f0bab-116">**PR_AB_DEFAULT_PAB** ([Pidtagabdefaultpab (](pidtagabdefaultpab-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f0bab-116">**PR_AB_DEFAULT_PAB** ([PidTagAbDefaultPab](pidtagabdefaultpab-canonical-property.md))</span></span>
    
<span data-ttu-id="f0bab-117">Diese drei Eigenschaften sind etwas Besonderes, da Sie nicht mit den standardmäßigen **IMAPIProp** -Methoden arbeiten können.</span><span class="sxs-lookup"><span data-stu-id="f0bab-117">These three properties are special because you cannot work with them using the standard **IMAPIProp** methods.</span></span> <span data-ttu-id="f0bab-118">Stattdessen müssen Sie **IAddrBook** -Methoden verwenden.</span><span class="sxs-lookup"><span data-stu-id="f0bab-118">Instead, you must use **IAddrBook** methods.</span></span> <span data-ttu-id="f0bab-119">Da keine dieser Eigenschaften mit **IMAPIProp::** SetProps geändert werden kann, ist es nicht erforderlich, **IMAPIProp:: SaveChanges** aufzurufen, um Änderungen dauerhaft vorzunehmen.</span><span class="sxs-lookup"><span data-stu-id="f0bab-119">Because none of these properties can be changed with **IMAPIProp::SetProps**, there is no need to call **IMAPIProp::SaveChanges** to make changes permanent.</span></span> <span data-ttu-id="f0bab-120">Änderungen, die über die **IAddrBook** -Methoden vorgenommen wurden, werden sofort wirksam.</span><span class="sxs-lookup"><span data-stu-id="f0bab-120">Modifications made through the **IAddrBook** methods take effect immediately.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f0bab-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f0bab-121">See also</span></span>



[<span data-ttu-id="f0bab-122">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="f0bab-122">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)

