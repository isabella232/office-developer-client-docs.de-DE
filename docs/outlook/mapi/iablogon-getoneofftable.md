---
title: IABLogonGetOneOffTable
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.GetOneOffTable
api_type:
- COM
ms.assetid: 7ac2a8d4-6890-4346-a6b6-34deca9dab50
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: b8a6d74df3749a5445d95ad392f7f88d27190bfc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791968"
---
# <a name="iablogongetoneofftable"></a><span data-ttu-id="5e35c-103">IABLogon::GetOneOffTable</span><span class="sxs-lookup"><span data-stu-id="5e35c-103">IABLogon::GetOneOffTable</span></span>

  
  
<span data-ttu-id="5e35c-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5e35c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5e35c-105">Gibt eine Tabelle mit einmaligen Vorlagen zum Erstellen von Empfängern, die Empfängerliste von ausgehenden Nachrichten hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="5e35c-105">Returns a table of one-off templates for creating recipients to be added to the recipient list of an outgoing message.</span></span>
  
```cpp
HRESULT GetOneOffTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="5e35c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5e35c-106">Parameters</span></span>

 <span data-ttu-id="5e35c-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="5e35c-107">_ulFlags_</span></span>
  
> <span data-ttu-id="5e35c-108">[in] Eine Bitmaske aus Flags, die den Typ der in der Tabelle enthaltenen Zeichenfolgenspalten steuert.</span><span class="sxs-lookup"><span data-stu-id="5e35c-108">[in] A bitmask of flags that controls the type of string columns included in the table.</span></span> <span data-ttu-id="5e35c-109">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="5e35c-109">The following flag can be set:</span></span>
    
<span data-ttu-id="5e35c-110">PARAMETER MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="5e35c-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="5e35c-111">Die Zeichenfolgenspalten sind im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="5e35c-111">The string columns are in Unicode format.</span></span> <span data-ttu-id="5e35c-112">Wenn die Option MAPI_UNICODE nicht festgelegt ist, werden die Zeichenfolgenspalten im ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="5e35c-112">If the MAPI_UNICODE flag is not set, the string columns are in ANSI format.</span></span>
    
 <span data-ttu-id="5e35c-113">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="5e35c-113">_lppTable_</span></span>
  
> <span data-ttu-id="5e35c-114">[out] Ein Zeiger auf einen Zeiger auf die einmaligen Tabelle.</span><span class="sxs-lookup"><span data-stu-id="5e35c-114">[out] A pointer to a pointer to the one-off table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="5e35c-115">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="5e35c-115">Return value</span></span>

<span data-ttu-id="5e35c-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="5e35c-116">S_OK</span></span> 
  
> <span data-ttu-id="5e35c-117">Die einmalige Tabelle wurde erfolgreich abgerufen.</span><span class="sxs-lookup"><span data-stu-id="5e35c-117">The one-off table was successfully retrieved.</span></span>
    
<span data-ttu-id="5e35c-118">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="5e35c-118">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="5e35c-119">Entweder die Option MAPI_UNICODE festgelegt wurde und die Adressbuchanbieter unterstützt keine Unicode oder Parameter MAPI_UNICODE wurde nicht festgelegt und die Adressbuchanbieter unterstützt nur Unicode.</span><span class="sxs-lookup"><span data-stu-id="5e35c-119">Either the MAPI_UNICODE flag was set and the address book provider does not support Unicode, or MAPI_UNICODE was not set and the address book provider supports only Unicode.</span></span>
    
<span data-ttu-id="5e35c-120">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="5e35c-120">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="5e35c-121">Der Adressbuchanbieter nicht einmal-Vorlagen zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="5e35c-121">The address book provider does not supply any one-off templates.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5e35c-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5e35c-122">Remarks</span></span>

<span data-ttu-id="5e35c-123">MAPI-Aufrufen die **GetOneOffTable** -Methode, um die verfügbare einmalige Vorlagen zum Erstellen von Empfängern tätigen.</span><span class="sxs-lookup"><span data-stu-id="5e35c-123">MAPI calls the **GetOneOffTable** method to make available one-off templates to create recipients.</span></span> <span data-ttu-id="5e35c-124">Die Empfängerliste von ausgehenden Nachrichten werden die neuen Empfänger hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="5e35c-124">The new recipients are added to the recipient list of an outgoing message.</span></span> <span data-ttu-id="5e35c-125">Von adressbuchanbietern implementierte sollte Benachrichtigung auf ihre einmaligen Tabelle um MAPI Vorlage Änderungen informieren zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="5e35c-125">Address book providers should support notification on their one-off table to inform MAPI of template modifications.</span></span> <span data-ttu-id="5e35c-126">MAPI bleibt die einmalige Tabelle geöffnet, um dynamische Aktualisieren zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="5e35c-126">MAPI keeps the one-off table open to enable dynamic updating.</span></span> 
  
<span data-ttu-id="5e35c-127">Von adressbuchanbietern implementierte können auch eine einmalige Tabelle für jeden ihrer Container unterstützen.</span><span class="sxs-lookup"><span data-stu-id="5e35c-127">Address book providers can also support a one-off table for each of their containers.</span></span> <span data-ttu-id="5e35c-128">Anrufer Abrufen dieser einmaligen Tabelle, des Containers [IMAPIProp::OpenProperty](imapiprop-openproperty.md) -Methode aufrufen und die Eigenschaft **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) anfordern.</span><span class="sxs-lookup"><span data-stu-id="5e35c-128">Callers retrieve this one-off table by calling the container's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method and requesting the **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) property.</span></span> <span data-ttu-id="5e35c-129">Über diese Tabelle verfügbaren Vorlagen dienen zum Empfänger zum Container hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="5e35c-129">The templates available through this table are used to add recipients to the container.</span></span> <span data-ttu-id="5e35c-130">Eine Erläuterung der Unterschiede zwischen den beiden Typen von einmaligen Tabellen finden Sie unter [Implementieren der einmaligen Tabellen](implementing-one-off-tables.md).</span><span class="sxs-lookup"><span data-stu-id="5e35c-130">For a discussion of the differences between the two types of one-off tables, see [Implementing One-Off Tables](implementing-one-off-tables.md).</span></span>
  
<span data-ttu-id="5e35c-131">Eine Übersicht über die erforderlichen Spalten in einer Adressbuchanbieter einmaligen Tabelle finden Sie unter [Einmaligen Tabellen](one-off-tables.md).</span><span class="sxs-lookup"><span data-stu-id="5e35c-131">For a list of the required columns in an address book provider's one-off table, see [One-Off Tables](one-off-tables.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="5e35c-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5e35c-132">See also</span></span>



[<span data-ttu-id="5e35c-133">IABContainer::CreateEntry</span><span class="sxs-lookup"><span data-stu-id="5e35c-133">IABContainer::CreateEntry</span></span>](iabcontainer-createentry.md)
  
[<span data-ttu-id="5e35c-134">IAddrBook::NewEntry</span><span class="sxs-lookup"><span data-stu-id="5e35c-134">IAddrBook::NewEntry</span></span>](iaddrbook-newentry.md)
  
[<span data-ttu-id="5e35c-135">IMAPISupport::GetOneOffTable</span><span class="sxs-lookup"><span data-stu-id="5e35c-135">IMAPISupport::GetOneOffTable</span></span>](imapisupport-getoneofftable.md)
  
[<span data-ttu-id="5e35c-136">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5e35c-136">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

