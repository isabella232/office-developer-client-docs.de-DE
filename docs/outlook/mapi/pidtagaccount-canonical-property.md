---
title: PidTagAccount (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAccount
api_type:
- HeaderDef
ms.assetid: bec199b5-abfd-4686-ad59-21092212e1a5
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 2962f973aa87b88f237ded69573df9ef312a7bc5
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25401104"
---
# <a name="pidtagaccount-canonical-property"></a><span data-ttu-id="29fad-103">PidTagAccount (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="29fad-103">PidTagAccount Canonical Property</span></span>

  
  
<span data-ttu-id="29fad-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="29fad-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="29fad-105">Der Name des Empfängers Konto enthält.</span><span class="sxs-lookup"><span data-stu-id="29fad-105">Contains the recipient's account name.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="29fad-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="29fad-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="29fad-107">PR_ACCOUNT, PR_ACCOUNT_A, PR_ACCOUNT_W</span><span class="sxs-lookup"><span data-stu-id="29fad-107">PR_ACCOUNT, PR_ACCOUNT_A, PR_ACCOUNT_W</span></span>  <br/> |
|<span data-ttu-id="29fad-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="29fad-108">Identifier:</span></span>  <br/> |<span data-ttu-id="29fad-109">0x3A00</span><span class="sxs-lookup"><span data-stu-id="29fad-109">0x3A00</span></span>  <br/> |
|<span data-ttu-id="29fad-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="29fad-110">Data type:</span></span>  <br/> |<span data-ttu-id="29fad-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="29fad-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="29fad-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="29fad-112">Area:</span></span>  <br/> |<span data-ttu-id="29fad-113">Adressbuch</span><span class="sxs-lookup"><span data-stu-id="29fad-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="29fad-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="29fad-114">Remarks</span></span>

<span data-ttu-id="29fad-115">Diese Eigenschaften Identitätsnachweis und Zugriff auf Informationen für einen Empfänger.</span><span class="sxs-lookup"><span data-stu-id="29fad-115">These properties provide identification and access information for a recipient.</span></span> <span data-ttu-id="29fad-116">Sie sind durch den Empfänger und ihre Organisation definiert.</span><span class="sxs-lookup"><span data-stu-id="29fad-116">They are defined by the recipient and their organization.</span></span>
  
<span data-ttu-id="29fad-117">Diese Eigenschaften enthalten häufig e-Mail-Namen des Empfängers, d. h., der letzten Komponente der e-Mail-Adresse an, die den Empfänger in der lokalen Organisation eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="29fad-117">These properties commonly contain the recipient's email name, that is, the final component of the email address, which uniquely identifies the recipient in the local organization.</span></span> <span data-ttu-id="29fad-118">Der e-Mail-Namen entspricht der x. 400-distinguished Name der einen kurzen Namen innerhalb einer bestimmten messaging Domäne eindeutig sein soll.</span><span class="sxs-lookup"><span data-stu-id="29fad-118">The email name corresponds to the X.400 distinguished name, which is meant to be a short name guaranteed to be unique within a certain messaging domain.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="29fad-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="29fad-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="29fad-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="29fad-120">Protocol specifications</span></span>

<span data-ttu-id="29fad-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="29fad-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="29fad-122">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="29fad-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="29fad-123">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="29fad-123">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="29fad-124">Gibt die Eigenschaften und Operationen, die für Kontakte und persönliche Verteilerlisten zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="29fad-124">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
<span data-ttu-id="29fad-125">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="29fad-125">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="29fad-126">Gibt die Eigenschaften und Operationen für Listen der Benutzer, Kontakte, Gruppen und Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="29fad-126">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="29fad-127">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="29fad-127">Header files</span></span>

<span data-ttu-id="29fad-128">mapitags.h</span><span class="sxs-lookup"><span data-stu-id="29fad-128">mapitags.h</span></span>
  
> <span data-ttu-id="29fad-129">Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="29fad-129">Contains definitions of properties listed as associated properties.</span></span>
    
<span data-ttu-id="29fad-130">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="29fad-130">mapidefs.h</span></span>
  
> <span data-ttu-id="29fad-131">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="29fad-131">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="29fad-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="29fad-132">See also</span></span>



[<span data-ttu-id="29fad-133">IMailUser : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="29fad-133">IMailUser : IMAPIProp</span></span>](imailuserimapiprop.md)


[<span data-ttu-id="29fad-134">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="29fad-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="29fad-135">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="29fad-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="29fad-136">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="29fad-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

