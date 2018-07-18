---
title: CONTAB_ENTRYID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 84251222-dac4-4f4d-97b9-aa0e2cd26c44
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 2c8661f24ed9555547446cf63fc08a3be7e6e941
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791436"
---
# <a name="contabentryid"></a><span data-ttu-id="0915d-103">CONTAB_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="0915d-103">CONTAB_ENTRYID</span></span>

  
  
<span data-ttu-id="0915d-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0915d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0915d-105">Enthält die Eintrags-ID für den Kontakteordner.</span><span class="sxs-lookup"><span data-stu-id="0915d-105">Contains the entry ID of the contacts folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0915d-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="0915d-106">Header file:</span></span>  <br/> |<span data-ttu-id="0915d-107">msomapiutil.h</span><span class="sxs-lookup"><span data-stu-id="0915d-107">msomapiutil.h</span></span>  <br/> |
   
```cpp
#pragma pack(4) 
typedef struct _contab_entryid
{
    BYTE abFlags[4];
    MAPIUID muid;
    ULONG ulVersion;
    ULONG ulType;
    ULONG ulIndex;
    ULONG cbeid;
    BYTE abeid[1];
}   CONTAB_ENTRYID, *LPCONTAB_ENTRYID;
#pragma pack() 
```

## <a name="members"></a><span data-ttu-id="0915d-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="0915d-108">Members</span></span>

 <span data-ttu-id="0915d-109">**abFlags**</span><span class="sxs-lookup"><span data-stu-id="0915d-109">**abFlags**</span></span>
  
> <span data-ttu-id="0915d-110">Eine Bitmaske aus Flags, die Informationen für das Objekt bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="0915d-110">A bitmask of flags that provides information describing the object.</span></span> <span data-ttu-id="0915d-111">Weitere Informationen finden Sie unter der Beschreibung des Felds **AbFlags** einer [ENTRYID](entryid.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="0915d-111">For more information, see the description of the **abFlags** field of an [ENTRYID](entryid.md) structure.</span></span> 
    
 <span data-ttu-id="0915d-112">**muid**</span><span class="sxs-lookup"><span data-stu-id="0915d-112">**muid**</span></span>
  
> <span data-ttu-id="0915d-113">GUID, den Speicheranbieter identifiziert.</span><span class="sxs-lookup"><span data-stu-id="0915d-113">GUID that identifies the store provider.</span></span>
    
 <span data-ttu-id="0915d-114">**ulVersion**</span><span class="sxs-lookup"><span data-stu-id="0915d-114">**ulVersion**</span></span>
  
> <span data-ttu-id="0915d-115">Die Versionsnummer der **CONTAB_ENTRYID** Struktur.</span><span class="sxs-lookup"><span data-stu-id="0915d-115">The version number of the **CONTAB_ENTRYID** structure.</span></span> <span data-ttu-id="0915d-116">Muss auf CONTAB_VERSION festgelegt sein.</span><span class="sxs-lookup"><span data-stu-id="0915d-116">Must be set to CONTAB_VERSION.</span></span> 
    
 <span data-ttu-id="0915d-117">**ulType**</span><span class="sxs-lookup"><span data-stu-id="0915d-117">**ulType**</span></span>
  
> <span data-ttu-id="0915d-118">Eine ganze Zahl, die den Kontakteintrag ID-Typ darstellt.</span><span class="sxs-lookup"><span data-stu-id="0915d-118">An integer representing the contact entry ID type.</span></span> <span data-ttu-id="0915d-119">Es muss eine der folgenden Werte sein:</span><span class="sxs-lookup"><span data-stu-id="0915d-119">It must be one of the following values:</span></span>
    
|<span data-ttu-id="0915d-120">**Name**</span><span class="sxs-lookup"><span data-stu-id="0915d-120">**Name**</span></span>|<span data-ttu-id="0915d-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0915d-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0915d-122">CONTAB_USER</span><span class="sxs-lookup"><span data-stu-id="0915d-122">CONTAB_USER</span></span>  <br/> |<span data-ttu-id="0915d-123">Ein messaging User-Objekt.</span><span class="sxs-lookup"><span data-stu-id="0915d-123">A messaging user object.</span></span>  <br/> |
|<span data-ttu-id="0915d-124">CONTAB_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="0915d-124">CONTAB_DISTLIST</span></span>  <br/> |<span data-ttu-id="0915d-125">Verteilung von List-Objekt.</span><span class="sxs-lookup"><span data-stu-id="0915d-125">A distribution list object.</span></span>  <br/> |
   
 <span data-ttu-id="0915d-126">**ulIndex**</span><span class="sxs-lookup"><span data-stu-id="0915d-126">**ulIndex**</span></span>
  
> <span data-ttu-id="0915d-127">Der Index der Teilmenge der e-Mail-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="0915d-127">The index into the email property subset.</span></span>
    
 <span data-ttu-id="0915d-128">**cbeid**</span><span class="sxs-lookup"><span data-stu-id="0915d-128">**cbeid**</span></span>
  
> <span data-ttu-id="0915d-129">Die Größe des Eintrags-ID der Nachricht Kontakt im Adressbuch Kontakte Eintrag zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="0915d-129">The size of the entry identifier of the Contact message associated with this entry in the Contacts Address Book.</span></span>
    
 <span data-ttu-id="0915d-130">**abeid**</span><span class="sxs-lookup"><span data-stu-id="0915d-130">**abeid**</span></span>
  
> <span data-ttu-id="0915d-131">Der Eintrag Bezeichner der Nachricht Kontakt im Adressbuch Kontakte Eintrag zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="0915d-131">The entry identifier of the Contact message associated with this entry in the Contacts Address Book.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0915d-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0915d-132">Remarks</span></span>

<span data-ttu-id="0915d-133">Einem Adressbuch Kontakte ist ein Adressbuch, das alle Kontaktelemente in einem Kontakteordner enthält, die eine e-Mail-Adresse oder eine Faxnummer verfügen.</span><span class="sxs-lookup"><span data-stu-id="0915d-133">A Contacts Address Book is an Address Book that contains all the contact items in a Contacts folder that have either an email address or a fax number.</span></span> <span data-ttu-id="0915d-134">Jeder Eintrag in einem Adressbuch Kontakte ist eine e-Mail-Adresse oder eine Faxnummer zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="0915d-134">Each entry in a Contacts Address Book is associated with either an email address or a fax number.</span></span> <span data-ttu-id="0915d-135">Da ein Kontaktelement kann bis zu drei e-Mail-Adressen und drei Faxnummer, kann ein Kontaktelement durch maximal sechs Einträge in der entsprechenden Kontaktadressbuch dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="0915d-135">Since a contact item can have up to three email addresses and three fax numbers, a contact item can be represented by up to six entries in the corresponding Contacts Address Book.</span></span>
  
<span data-ttu-id="0915d-136">Einem Adressbuch Kontakte dient zur Unterstützung von Benutzern, die Adressierung von e-Mail-Nachrichten an Kontakte in einem Kontakteordner.</span><span class="sxs-lookup"><span data-stu-id="0915d-136">The purpose of a Contacts Address Book is to support users addressing email messages to contacts in a Contacts folder.</span></span> <span data-ttu-id="0915d-137">Der Adressbuch Kontakte-Anbieter, die Unterstützung von Microsoft Outlook 2010 und Microsoft Outlook 2013 ist contab32.dll.</span><span class="sxs-lookup"><span data-stu-id="0915d-137">The Contacts Address Book provider that Microsoft Outlook 2010 and Microsoft Outlook 2013 support is contab32.dll.</span></span>
  
<span data-ttu-id="0915d-138">Die Struktur **CONTAB_ENTRYID** unterstützt eine Teilmenge der Informationen, die in der zugrunde liegenden MAPI-Kontakt Nachricht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="0915d-138">The **CONTAB_ENTRYID** structure supports a subset of the information that is present in the underlying MAPI Contact message.</span></span> <span data-ttu-id="0915d-139">Identifiziert die Kontakt-Nachricht, der ein bestimmter Eintrag Adressbuch Kontakte zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="0915d-139">It identifies the Contact message that a particular Contacts Address Book entry is associated with.</span></span> 
  
<span data-ttu-id="0915d-140">Die Felder **Cbeid** und **Abeid** sind nur gültig, wenn der Wert des Felds **UlType** auf CONTAB_DISTLIST oder CONTAB_USER festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="0915d-140">The **cbeid** and **abeid** fields are only valid when the **ulType** field value is set to CONTAB_DISTLIST or CONTAB_USER.</span></span> <span data-ttu-id="0915d-141">Wenn der Wert des Felds **UlType** CONTAB_ROOT, CONTAB_SUBROOT oder CONTAB_CONTAINER festgelegt ist, sollte die Struktur [DIR_ENTRYID](dir_entryid.md) stattdessen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0915d-141">When the **ulType** field value is set to CONTAB_ROOT, CONTAB_SUBROOT, or CONTAB_CONTAINER, the [DIR_ENTRYID](dir_entryid.md) structure should be used instead.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0915d-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0915d-142">See also</span></span>



[<span data-ttu-id="0915d-143">DIR_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="0915d-143">DIR_ENTRYID</span></span>](dir_entryid.md)


[<span data-ttu-id="0915d-144">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="0915d-144">MAPI Structures</span></span>](mapi-structures.md)

