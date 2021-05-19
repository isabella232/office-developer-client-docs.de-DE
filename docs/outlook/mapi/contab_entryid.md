---
title: CONTAB_ENTRYID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 84251222-dac4-4f4d-97b9-aa0e2cd26c44
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: a2a204f76b62c8c6bc6d8a4e793c936a0184dc65
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424084"
---
# <a name="contab_entryid"></a><span data-ttu-id="05253-103">CONTAB_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="05253-103">CONTAB_ENTRYID</span></span>

  
  
<span data-ttu-id="05253-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="05253-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="05253-105">Enthält die Eintrags-ID des Kontaktordners.</span><span class="sxs-lookup"><span data-stu-id="05253-105">Contains the entry ID of the contacts folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="05253-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="05253-106">Header file:</span></span>  <br/> |<span data-ttu-id="05253-107">msomapiutil.h</span><span class="sxs-lookup"><span data-stu-id="05253-107">msomapiutil.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="05253-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="05253-108">Members</span></span>

 <span data-ttu-id="05253-109">**abFlags**</span><span class="sxs-lookup"><span data-stu-id="05253-109">**abFlags**</span></span>
  
> <span data-ttu-id="05253-110">Eine Bitmaske mit Flags, die Informationen zur Beschreibung des Objekts enthält.</span><span class="sxs-lookup"><span data-stu-id="05253-110">A bitmask of flags that provides information describing the object.</span></span> <span data-ttu-id="05253-111">Weitere Informationen finden Sie in der Beschreibung des **AbFlags-Felds** einer [ENTRYID-Struktur.](entryid.md)</span><span class="sxs-lookup"><span data-stu-id="05253-111">For more information, see the description of the **abFlags** field of an [ENTRYID](entryid.md) structure.</span></span> 
    
 <span data-ttu-id="05253-112">**muid**</span><span class="sxs-lookup"><span data-stu-id="05253-112">**muid**</span></span>
  
> <span data-ttu-id="05253-113">GUID, die den Speicheranbieter identifiziert.</span><span class="sxs-lookup"><span data-stu-id="05253-113">GUID that identifies the store provider.</span></span>
    
 <span data-ttu-id="05253-114">**ulVersion**</span><span class="sxs-lookup"><span data-stu-id="05253-114">**ulVersion**</span></span>
  
> <span data-ttu-id="05253-115">Die Versionsnummer der **CONTAB_ENTRYID** Struktur.</span><span class="sxs-lookup"><span data-stu-id="05253-115">The version number of the **CONTAB_ENTRYID** structure.</span></span> <span data-ttu-id="05253-116">Muss auf CONTAB_VERSION.</span><span class="sxs-lookup"><span data-stu-id="05253-116">Must be set to CONTAB_VERSION.</span></span> 
    
 <span data-ttu-id="05253-117">**ulType**</span><span class="sxs-lookup"><span data-stu-id="05253-117">**ulType**</span></span>
  
> <span data-ttu-id="05253-118">Eine ganze Zahl, die den Kontakteintrags-ID-Typ darstellt.</span><span class="sxs-lookup"><span data-stu-id="05253-118">An integer representing the contact entry ID type.</span></span> <span data-ttu-id="05253-119">Dies muss einer der folgenden Werte sein:</span><span class="sxs-lookup"><span data-stu-id="05253-119">It must be one of the following values:</span></span>
    
|<span data-ttu-id="05253-120">**Name**</span><span class="sxs-lookup"><span data-stu-id="05253-120">**Name**</span></span>|<span data-ttu-id="05253-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="05253-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="05253-122">CONTAB_USER</span><span class="sxs-lookup"><span data-stu-id="05253-122">CONTAB_USER</span></span>  <br/> |<span data-ttu-id="05253-123">Ein Nachrichtenbenutzer-Objekt.</span><span class="sxs-lookup"><span data-stu-id="05253-123">A messaging user object.</span></span>  <br/> |
|<span data-ttu-id="05253-124">CONTAB_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="05253-124">CONTAB_DISTLIST</span></span>  <br/> |<span data-ttu-id="05253-125">Verteilung von List-Objekt.</span><span class="sxs-lookup"><span data-stu-id="05253-125">A distribution list object.</span></span>  <br/> |
   
 <span data-ttu-id="05253-126">**ulIndex**</span><span class="sxs-lookup"><span data-stu-id="05253-126">**ulIndex**</span></span>
  
> <span data-ttu-id="05253-127">Der Index in die Teilmenge der E-Mail-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="05253-127">The index into the email property subset.</span></span>
    
 <span data-ttu-id="05253-128">**cbeid**</span><span class="sxs-lookup"><span data-stu-id="05253-128">**cbeid**</span></span>
  
> <span data-ttu-id="05253-129">Die Größe der Eintrags-ID der Kontaktnachricht, die diesem Eintrag im Adressbuch kontakte zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="05253-129">The size of the entry identifier of the Contact message associated with this entry in the Contacts Address Book.</span></span>
    
 <span data-ttu-id="05253-130">**abeid**</span><span class="sxs-lookup"><span data-stu-id="05253-130">**abeid**</span></span>
  
> <span data-ttu-id="05253-131">Der Eintragsbezeichner der Kontaktnachricht, die diesem Eintrag im Adressbuch "Kontakte" zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="05253-131">The entry identifier of the Contact message associated with this entry in the Contacts Address Book.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="05253-132">Hinweise</span><span class="sxs-lookup"><span data-stu-id="05253-132">Remarks</span></span>

<span data-ttu-id="05253-133">Ein Kontakt-Adressbuch ist ein Adressbuch, das alle Kontaktelemente in einem Kontaktordner enthält, die entweder eine E-Mail-Adresse oder eine Faxnummer haben.</span><span class="sxs-lookup"><span data-stu-id="05253-133">A Contacts Address Book is an Address Book that contains all the contact items in a Contacts folder that have either an email address or a fax number.</span></span> <span data-ttu-id="05253-134">Jeder Eintrag in einem Adressbuch für Kontakte ist entweder einer E-Mail-Adresse oder einer Faxnummer zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="05253-134">Each entry in a Contacts Address Book is associated with either an email address or a fax number.</span></span> <span data-ttu-id="05253-135">Da ein Kontaktelement bis zu drei E-Mail-Adressen und drei Faxnummern haben kann, kann ein Kontaktelement durch bis zu sechs Einträge im entsprechenden Kontaktadressenbuch dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="05253-135">Since a contact item can have up to three email addresses and three fax numbers, a contact item can be represented by up to six entries in the corresponding Contacts Address Book.</span></span>
  
<span data-ttu-id="05253-136">Der Zweck eines Adressbuchs für Kontakte besteht in der Unterstützung von Benutzern, die E-Mail-Nachrichten an Kontakte in einem Kontaktordner adressieren.</span><span class="sxs-lookup"><span data-stu-id="05253-136">The purpose of a Contacts Address Book is to support users addressing email messages to contacts in a Contacts folder.</span></span> <span data-ttu-id="05253-137">Der Adressbuchanbieter für Kontakte, der Microsoft Outlook 2010 und Microsoft Outlook 2013 unterstützt, wird contab32.dll.</span><span class="sxs-lookup"><span data-stu-id="05253-137">The Contacts Address Book provider that Microsoft Outlook 2010 and Microsoft Outlook 2013 support is contab32.dll.</span></span>
  
<span data-ttu-id="05253-138">Die **CONTAB_ENTRYID** unterstützt eine Teilmenge der Informationen, die in der zugrunde liegenden MAPI-Kontaktnachricht vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="05253-138">The **CONTAB_ENTRYID** structure supports a subset of the information that is present in the underlying MAPI Contact message.</span></span> <span data-ttu-id="05253-139">Es identifiziert die Kontaktnachricht, der ein bestimmter Kontakt-Adressbucheintrag zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="05253-139">It identifies the Contact message that a particular Contacts Address Book entry is associated with.</span></span> 
  
<span data-ttu-id="05253-140">Die **Felder cbeid** und **abeid** sind nur gültig, wenn der **ulType-Feldwert** auf CONTAB_DISTLIST oder CONTAB_USER.</span><span class="sxs-lookup"><span data-stu-id="05253-140">The **cbeid** and **abeid** fields are only valid when the **ulType** field value is set to CONTAB_DISTLIST or CONTAB_USER.</span></span> <span data-ttu-id="05253-141">Wenn der wert des **ulType-Felds** auf CONTAB_ROOT, CONTAB_SUBROOT oder CONTAB_CONTAINER festgelegt ist, sollte stattdessen [DIR_ENTRYID](dir_entryid.md) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="05253-141">When the **ulType** field value is set to CONTAB_ROOT, CONTAB_SUBROOT, or CONTAB_CONTAINER, the [DIR_ENTRYID](dir_entryid.md) structure should be used instead.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="05253-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="05253-142">See also</span></span>



[<span data-ttu-id="05253-143">DIR_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="05253-143">DIR_ENTRYID</span></span>](dir_entryid.md)


[<span data-ttu-id="05253-144">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="05253-144">MAPI Structures</span></span>](mapi-structures.md)

