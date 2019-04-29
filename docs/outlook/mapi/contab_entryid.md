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
# <a name="contabentryid"></a><span data-ttu-id="de766-103">CONTAB_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="de766-103">CONTAB_ENTRYID</span></span>

  
  
<span data-ttu-id="de766-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="de766-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="de766-105">Enthält die Eintrags-ID des Ordners Kontakte.</span><span class="sxs-lookup"><span data-stu-id="de766-105">Contains the entry ID of the contacts folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="de766-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="de766-106">Header file:</span></span>  <br/> |<span data-ttu-id="de766-107">msomapiutil. h</span><span class="sxs-lookup"><span data-stu-id="de766-107">msomapiutil.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="de766-108">Members</span><span class="sxs-lookup"><span data-stu-id="de766-108">Members</span></span>

 <span data-ttu-id="de766-109">**abFlags**</span><span class="sxs-lookup"><span data-stu-id="de766-109">**abFlags**</span></span>
  
> <span data-ttu-id="de766-110">Eine Bitmaske von Flags, die Informationen zur Beschreibung des Objekts bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="de766-110">A bitmask of flags that provides information describing the object.</span></span> <span data-ttu-id="de766-111">Weitere Informationen finden Sie in der Beschreibung des **abFlags** -Felds einer [Eintrags](entryid.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="de766-111">For more information, see the description of the **abFlags** field of an [ENTRYID](entryid.md) structure.</span></span> 
    
 <span data-ttu-id="de766-112">**muid**</span><span class="sxs-lookup"><span data-stu-id="de766-112">**muid**</span></span>
  
> <span data-ttu-id="de766-113">GUID, die den Informationsspeicher Anbieter identifiziert.</span><span class="sxs-lookup"><span data-stu-id="de766-113">GUID that identifies the store provider.</span></span>
    
 <span data-ttu-id="de766-114">**ulVersion**</span><span class="sxs-lookup"><span data-stu-id="de766-114">**ulVersion**</span></span>
  
> <span data-ttu-id="de766-115">Die Versionsnummer der **CONTAB_ENTRYID** -Struktur.</span><span class="sxs-lookup"><span data-stu-id="de766-115">The version number of the **CONTAB_ENTRYID** structure.</span></span> <span data-ttu-id="de766-116">Muss auf CONTAB_VERSION festgelegt sein.</span><span class="sxs-lookup"><span data-stu-id="de766-116">Must be set to CONTAB_VERSION.</span></span> 
    
 <span data-ttu-id="de766-117">**ulType**</span><span class="sxs-lookup"><span data-stu-id="de766-117">**ulType**</span></span>
  
> <span data-ttu-id="de766-118">Eine ganze Zahl, die den Typ des Kontakteintrags darstellt.</span><span class="sxs-lookup"><span data-stu-id="de766-118">An integer representing the contact entry ID type.</span></span> <span data-ttu-id="de766-119">Dabei muss es sich um einen der folgenden Werte handeln:</span><span class="sxs-lookup"><span data-stu-id="de766-119">It must be one of the following values:</span></span>
    
|<span data-ttu-id="de766-120">**Name**</span><span class="sxs-lookup"><span data-stu-id="de766-120">**Name**</span></span>|<span data-ttu-id="de766-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="de766-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="de766-122">CONTAB_USER</span><span class="sxs-lookup"><span data-stu-id="de766-122">CONTAB_USER</span></span>  <br/> |<span data-ttu-id="de766-123">Ein Nachrichtenbenutzer-Objekt.</span><span class="sxs-lookup"><span data-stu-id="de766-123">A messaging user object.</span></span>  <br/> |
|<span data-ttu-id="de766-124">CONTAB_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="de766-124">CONTAB_DISTLIST</span></span>  <br/> |<span data-ttu-id="de766-125">Verteilung von List-Objekt.</span><span class="sxs-lookup"><span data-stu-id="de766-125">A distribution list object.</span></span>  <br/> |
   
 <span data-ttu-id="de766-126">**ulIndex**</span><span class="sxs-lookup"><span data-stu-id="de766-126">**ulIndex**</span></span>
  
> <span data-ttu-id="de766-127">Der Index in der e-Mail-Eigenschaft-Teilmenge.</span><span class="sxs-lookup"><span data-stu-id="de766-127">The index into the email property subset.</span></span>
    
 <span data-ttu-id="de766-128">**cbeid**</span><span class="sxs-lookup"><span data-stu-id="de766-128">**cbeid**</span></span>
  
> <span data-ttu-id="de766-129">Die Größe der Eintrags-ID der Kontakt Nachricht, die diesem Eintrag im Adressbuchkontakte zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="de766-129">The size of the entry identifier of the Contact message associated with this entry in the Contacts Address Book.</span></span>
    
 <span data-ttu-id="de766-130">**Abeid**</span><span class="sxs-lookup"><span data-stu-id="de766-130">**abeid**</span></span>
  
> <span data-ttu-id="de766-131">Die Eintrags-ID der Kontakt Nachricht, die diesem Eintrag im Adressbuchkontakte zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="de766-131">The entry identifier of the Contact message associated with this entry in the Contacts Address Book.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="de766-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="de766-132">Remarks</span></span>

<span data-ttu-id="de766-133">Ein Adressbuch für Kontakte ist ein Adressbuch, das alle Kontaktelemente in einem Kontakteordner enthält, die entweder eine e-Mail-Adresse oder eine Faxnummer enthalten.</span><span class="sxs-lookup"><span data-stu-id="de766-133">A Contacts Address Book is an Address Book that contains all the contact items in a Contacts folder that have either an email address or a fax number.</span></span> <span data-ttu-id="de766-134">Jeder Eintrag in einem Contacts-Adressbuch ist entweder einer e-Mail-Adresse oder einer Faxnummer zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="de766-134">Each entry in a Contacts Address Book is associated with either an email address or a fax number.</span></span> <span data-ttu-id="de766-135">Da ein Kontaktelement bis zu drei e-Mail-Adressen und drei Faxnummern enthalten kann, kann ein Kontaktelement durch bis zu sechs Einträge im entsprechenden Adressbuch für Kontakte dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="de766-135">Since a contact item can have up to three email addresses and three fax numbers, a contact item can be represented by up to six entries in the corresponding Contacts Address Book.</span></span>
  
<span data-ttu-id="de766-136">Der Zweck eines Kontakt Adressbuchs besteht darin, Benutzer zu unterstützen, die e-Mail-Nachrichten an Kontakte in einem Kontakteordner adressieren.</span><span class="sxs-lookup"><span data-stu-id="de766-136">The purpose of a Contacts Address Book is to support users addressing email messages to contacts in a Contacts folder.</span></span> <span data-ttu-id="de766-137">Der Adressbuchanbieter für Kontakte, der von Microsoft Outlook 2010 und Microsoft Outlook 2013 unterstützt wird, ist contab32. dll.</span><span class="sxs-lookup"><span data-stu-id="de766-137">The Contacts Address Book provider that Microsoft Outlook 2010 and Microsoft Outlook 2013 support is contab32.dll.</span></span>
  
<span data-ttu-id="de766-138">Die **CONTAB_ENTRYID** -Struktur unterstützt eine Teilmenge der Informationen, die in der zugrunde liegenden MAPI-Kontakt Nachricht enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="de766-138">The **CONTAB_ENTRYID** structure supports a subset of the information that is present in the underlying MAPI Contact message.</span></span> <span data-ttu-id="de766-139">Sie identifiziert die Kontakt Nachricht, der ein bestimmter Adressbucheintrag für Kontakte zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="de766-139">It identifies the Contact message that a particular Contacts Address Book entry is associated with.</span></span> 
  
<span data-ttu-id="de766-140">Die Felder **cbeid** und **Abeid** sind nur gültig, wenn der **ulType** -Feldwert auf CONTAB_DISTLIST oder CONTAB_USER festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="de766-140">The **cbeid** and **abeid** fields are only valid when the **ulType** field value is set to CONTAB_DISTLIST or CONTAB_USER.</span></span> <span data-ttu-id="de766-141">Wenn der **ulType** -FELDWERT auf CONTAB_ROOT, CONTAB_SUBROOT oder CONTAB_CONTAINER festgelegt ist, sollte stattdessen die [DIR_ENTRYID](dir_entryid.md) -Struktur verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="de766-141">When the **ulType** field value is set to CONTAB_ROOT, CONTAB_SUBROOT, or CONTAB_CONTAINER, the [DIR_ENTRYID](dir_entryid.md) structure should be used instead.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="de766-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="de766-142">See also</span></span>



[<span data-ttu-id="de766-143">DIR_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="de766-143">DIR_ENTRYID</span></span>](dir_entryid.md)


[<span data-ttu-id="de766-144">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="de766-144">MAPI Structures</span></span>](mapi-structures.md)

