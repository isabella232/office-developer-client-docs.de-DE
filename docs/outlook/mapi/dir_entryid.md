---
title: DIR_ENTRYID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9e055269-f3bf-4b64-8384-3cbc372c0b34
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 2af9d529cb92e1040427eba69270908dcf4a5d9f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791557"
---
# <a name="direntryid"></a><span data-ttu-id="22faf-103">DIR_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="22faf-103">DIR_ENTRYID</span></span>

  
  
<span data-ttu-id="22faf-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="22faf-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="22faf-105">Beschreibt die Eigenschaften einer Directory-Eintrags-ID an.</span><span class="sxs-lookup"><span data-stu-id="22faf-105">Describes the properties of a directory entry id.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="22faf-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="22faf-106">Header file:</span></span>  <br/> |<span data-ttu-id="22faf-107">EntryID.h</span><span class="sxs-lookup"><span data-stu-id="22faf-107">entryid.h</span></span>  <br/> |
   
```cpp
#pragma pack(4)
typedef struct _dir_entryid
{
    BYTE abFlags[4]; 
    MAPIUID muid; 
    ULONG ulVersion; 
    ULONG ulType; 
    MAPIUID muidID; 
}   DIR_ENTRYID, *LPDIR_ENTRYID; 
#pragma pack()
```

## <a name="members"></a><span data-ttu-id="22faf-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="22faf-108">Members</span></span>

 <span data-ttu-id="22faf-109">**abFlags**</span><span class="sxs-lookup"><span data-stu-id="22faf-109">**abFlags**</span></span>
  
> <span data-ttu-id="22faf-110">Eine Bitmaske aus Flags, die Informationen für das Objekt bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="22faf-110">A bitmask of flags that provides information describing the object.</span></span> <span data-ttu-id="22faf-111">Weitere Informationen finden Sie unter der Beschreibung des Felds **AbFlags** einer [ENTRYID](entryid.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="22faf-111">For more information, see the description of the **abFlags** field of an [ENTRYID](entryid.md) structure.</span></span> 
    
 <span data-ttu-id="22faf-112">**muid**</span><span class="sxs-lookup"><span data-stu-id="22faf-112">**muid**</span></span>
  
> <span data-ttu-id="22faf-113">GUID, den Speicheranbieter identifiziert.</span><span class="sxs-lookup"><span data-stu-id="22faf-113">GUID that identifies the store provider.</span></span>
    
 <span data-ttu-id="22faf-114">**ulVersion**</span><span class="sxs-lookup"><span data-stu-id="22faf-114">**ulVersion**</span></span>
  
> <span data-ttu-id="22faf-115">Die Versionsnummer der **DIR_ENTRYID** Struktur.</span><span class="sxs-lookup"><span data-stu-id="22faf-115">The version number of the **DIR_ENTRYID** structure.</span></span> <span data-ttu-id="22faf-116">Muss auf CONTAB_VERSION festgelegt sein.</span><span class="sxs-lookup"><span data-stu-id="22faf-116">Must be set to CONTAB_VERSION.</span></span> 
    
 <span data-ttu-id="22faf-117">**ulType**</span><span class="sxs-lookup"><span data-stu-id="22faf-117">**ulType**</span></span>
  
> <span data-ttu-id="22faf-118">Eine ganze Zahl, die die Art des Directory-Eintrags-ID darstellt.</span><span class="sxs-lookup"><span data-stu-id="22faf-118">An integer representing the directory entry ID type.</span></span> <span data-ttu-id="22faf-119">Es muss eine der folgenden Werte sein:</span><span class="sxs-lookup"><span data-stu-id="22faf-119">It must be one of the following values:</span></span>
    
|<span data-ttu-id="22faf-120">**Name**</span><span class="sxs-lookup"><span data-stu-id="22faf-120">**Name**</span></span>|<span data-ttu-id="22faf-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="22faf-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="22faf-122">CONTAB_ROOT</span><span class="sxs-lookup"><span data-stu-id="22faf-122">CONTAB_ROOT</span></span>  <br/> |<span data-ttu-id="22faf-123">Der Stammordner für einen MAPI-Adressbuch.</span><span class="sxs-lookup"><span data-stu-id="22faf-123">The root folder for a MAPI address book.</span></span>  <br/> |
|<span data-ttu-id="22faf-124">CONTAB_SUBROOT</span><span class="sxs-lookup"><span data-stu-id="22faf-124">CONTAB_SUBROOT</span></span>  <br/> |<span data-ttu-id="22faf-125">Ein Unterordner in den Stammordner des MAPI-Address Book-Objekts enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="22faf-125">A subfolder contained within the root folder of the MAPI address book object.</span></span>  <br/> |
|<span data-ttu-id="22faf-126">CONTAB_CONTAINER</span><span class="sxs-lookup"><span data-stu-id="22faf-126">CONTAB_CONTAINER</span></span>  <br/> |<span data-ttu-id="22faf-127">Ein Address Book Container-Objekt.</span><span class="sxs-lookup"><span data-stu-id="22faf-127">An address book container object.</span></span>  <br/> |
   
 <span data-ttu-id="22faf-128">**muidID**</span><span class="sxs-lookup"><span data-stu-id="22faf-128">**muidID**</span></span>
  
> <span data-ttu-id="22faf-129">Eine GUID, die das Anmeldung-Objekt identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="22faf-129">A GUID that identifies the logon object.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="22faf-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="22faf-130">Remarks</span></span>

<span data-ttu-id="22faf-131">Die Strukturen **DIR_ENTRYID** und [CONTAB_ENTRYID](contab_entryid.md) sind identisch, mit Ausnahme der **UlType** Member.</span><span class="sxs-lookup"><span data-stu-id="22faf-131">The structures **DIR_ENTRYID** and [CONTAB_ENTRYID](contab_entryid.md) are identical, except for the **ulType** member.</span></span> <span data-ttu-id="22faf-132">Der Inhalt des Elements **UlType** bestimmt, welche Struktur für die übrigen Felder geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="22faf-132">The contents of the **ulType** member determine which structure is appropriate for the remaining fields.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="22faf-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="22faf-133">See also</span></span>



[<span data-ttu-id="22faf-134">CONTAB_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="22faf-134">CONTAB_ENTRYID</span></span>](contab_entryid.md)


[<span data-ttu-id="22faf-135">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="22faf-135">MAPI Structures</span></span>](mapi-structures.md)

