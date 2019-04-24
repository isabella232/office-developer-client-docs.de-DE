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
ms.openlocfilehash: e7abcb2c86ff5cabe0b8f5664ec316244617ac09
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316674"
---
# <a name="direntryid"></a><span data-ttu-id="5d8e6-103">DIR_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="5d8e6-103">DIR_ENTRYID</span></span>

  
  
<span data-ttu-id="5d8e6-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5d8e6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5d8e6-105">Beschreibt die Eigenschaften einer Verzeichniseintrags-ID.</span><span class="sxs-lookup"><span data-stu-id="5d8e6-105">Describes the properties of a directory entry id.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5d8e6-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="5d8e6-106">Header file:</span></span>  <br/> |<span data-ttu-id="5d8e6-107">Eintrags-Nr. h</span><span class="sxs-lookup"><span data-stu-id="5d8e6-107">entryid.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="5d8e6-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="5d8e6-108">Members</span></span>

 <span data-ttu-id="5d8e6-109">**abFlags**</span><span class="sxs-lookup"><span data-stu-id="5d8e6-109">**abFlags**</span></span>
  
> <span data-ttu-id="5d8e6-110">Eine Bitmaske von Flags, die Informationen zur Beschreibung des Objekts bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="5d8e6-110">A bitmask of flags that provides information describing the object.</span></span> <span data-ttu-id="5d8e6-111">Weitere Informationen finden Sie in der Beschreibung des **abFlags** -Felds einer [Eintrags](entryid.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="5d8e6-111">For more information, see the description of the **abFlags** field of an [ENTRYID](entryid.md) structure.</span></span> 
    
 <span data-ttu-id="5d8e6-112">**muid**</span><span class="sxs-lookup"><span data-stu-id="5d8e6-112">**muid**</span></span>
  
> <span data-ttu-id="5d8e6-113">GUID, die den Informationsspeicher Anbieter identifiziert.</span><span class="sxs-lookup"><span data-stu-id="5d8e6-113">GUID that identifies the store provider.</span></span>
    
 <span data-ttu-id="5d8e6-114">**ulVersion**</span><span class="sxs-lookup"><span data-stu-id="5d8e6-114">**ulVersion**</span></span>
  
> <span data-ttu-id="5d8e6-115">Die Versionsnummer der **DIR_ENTRYID** -Struktur.</span><span class="sxs-lookup"><span data-stu-id="5d8e6-115">The version number of the **DIR_ENTRYID** structure.</span></span> <span data-ttu-id="5d8e6-116">Muss auf CONTAB_VERSION festgelegt sein.</span><span class="sxs-lookup"><span data-stu-id="5d8e6-116">Must be set to CONTAB_VERSION.</span></span> 
    
 <span data-ttu-id="5d8e6-117">**ulType**</span><span class="sxs-lookup"><span data-stu-id="5d8e6-117">**ulType**</span></span>
  
> <span data-ttu-id="5d8e6-118">Eine ganze Zahl, die den Verzeichniseintrags-ID-Typ darstellt.</span><span class="sxs-lookup"><span data-stu-id="5d8e6-118">An integer representing the directory entry ID type.</span></span> <span data-ttu-id="5d8e6-119">Dabei muss es sich um einen der folgenden Werte handeln:</span><span class="sxs-lookup"><span data-stu-id="5d8e6-119">It must be one of the following values:</span></span>
    
|<span data-ttu-id="5d8e6-120">**Name**</span><span class="sxs-lookup"><span data-stu-id="5d8e6-120">**Name**</span></span>|<span data-ttu-id="5d8e6-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5d8e6-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5d8e6-122">CONTAB_ROOT</span><span class="sxs-lookup"><span data-stu-id="5d8e6-122">CONTAB_ROOT</span></span>  <br/> |<span data-ttu-id="5d8e6-123">Der Stammordner für ein MAPI-Adressbuch.</span><span class="sxs-lookup"><span data-stu-id="5d8e6-123">The root folder for a MAPI address book.</span></span>  <br/> |
|<span data-ttu-id="5d8e6-124">CONTAB_SUBROOT</span><span class="sxs-lookup"><span data-stu-id="5d8e6-124">CONTAB_SUBROOT</span></span>  <br/> |<span data-ttu-id="5d8e6-125">Ein im Stammordner des MAPI-Adressbuch-Objekts enthaltener Unterordner.</span><span class="sxs-lookup"><span data-stu-id="5d8e6-125">A subfolder contained within the root folder of the MAPI address book object.</span></span>  <br/> |
|<span data-ttu-id="5d8e6-126">CONTAB_CONTAINER</span><span class="sxs-lookup"><span data-stu-id="5d8e6-126">CONTAB_CONTAINER</span></span>  <br/> |<span data-ttu-id="5d8e6-127">Ein Address Book Container-Objekt.</span><span class="sxs-lookup"><span data-stu-id="5d8e6-127">An address book container object.</span></span>  <br/> |
   
 <span data-ttu-id="5d8e6-128">**muidID**</span><span class="sxs-lookup"><span data-stu-id="5d8e6-128">**muidID**</span></span>
  
> <span data-ttu-id="5d8e6-129">Eine GUID, die das Logon-Objekt identifiziert.</span><span class="sxs-lookup"><span data-stu-id="5d8e6-129">A GUID that identifies the logon object.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5d8e6-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5d8e6-130">Remarks</span></span>

<span data-ttu-id="5d8e6-131">Die Strukturen **DIR_ENTRYID** und [CONTAB_ENTRYID](contab_entryid.md) sind identisch, mit Ausnahme des **ulType** -Elements.</span><span class="sxs-lookup"><span data-stu-id="5d8e6-131">The structures **DIR_ENTRYID** and [CONTAB_ENTRYID](contab_entryid.md) are identical, except for the **ulType** member.</span></span> <span data-ttu-id="5d8e6-132">Der Inhalt des **ulType** -Elements bestimmt, welche Struktur für die verbleibenden Felder geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="5d8e6-132">The contents of the **ulType** member determine which structure is appropriate for the remaining fields.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5d8e6-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5d8e6-133">See also</span></span>



[<span data-ttu-id="5d8e6-134">CONTAB_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="5d8e6-134">CONTAB_ENTRYID</span></span>](contab_entryid.md)


[<span data-ttu-id="5d8e6-135">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="5d8e6-135">MAPI Structures</span></span>](mapi-structures.md)

