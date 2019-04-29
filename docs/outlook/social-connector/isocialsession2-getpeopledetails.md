---
title: ISocialSession2GetPeopleDetails
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8733aab9-3a8e-4924-b62f-4e871d991c72
description: Gibt eine Zeichenfolge, die eine Auflistung von Personen-und Bilddetails für die durch den personsAddresses-Parameter angegebenen Benutzer enthält.
ms.openlocfilehash: 08b6eca193da59bbdc3c9d21d4dc9b6d0e0c884f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404533"
---
# <a name="isocialsession2getpeopledetails"></a><span data-ttu-id="03853-103">ISocialSession2::GetPeopleDetails</span><span class="sxs-lookup"><span data-stu-id="03853-103">ISocialSession2::GetPeopleDetails</span></span>

<span data-ttu-id="03853-104">Gibt eine Zeichenfolge, die eine Auflistung von Personen-und Bilddetails für die durch den _personsAddresses_ -Parameter angegebenen Benutzer enthält.</span><span class="sxs-lookup"><span data-stu-id="03853-104">Returns a string that contains a collection of person and picture details for the users specified by the  _personsAddresses_ parameter.</span></span> 
  
```cpp
HRESULT _stdcall GetPeopleDetails([in] BSTR personsAddresses, [out, retval] BSTR* personsCollection);
```

## <a name="parameters"></a><span data-ttu-id="03853-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="03853-105">Parameters</span></span>

<span data-ttu-id="03853-106">_personsAddresses_</span><span class="sxs-lookup"><span data-stu-id="03853-106">_personsAddresses_</span></span>
  
> <span data-ttu-id="03853-107">in Eine XML-Zeichenfolge, die die Hash-SMTP-Adressen einer Gruppe von Benutzern angibt.</span><span class="sxs-lookup"><span data-stu-id="03853-107">[in] An XML string that specifies the hashed SMTP addresses of a set of users.</span></span>
    
<span data-ttu-id="03853-108">_personencollection_</span><span class="sxs-lookup"><span data-stu-id="03853-108">_personsCollection_</span></span>
  
> <span data-ttu-id="03853-109">Out Eine XML-Zeichenfolge, die eine Auflistung von Personen-und Bilddetails enthält.</span><span class="sxs-lookup"><span data-stu-id="03853-109">[out] An XML string that contains a collection of person and picture details.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="03853-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="03853-110">Remarks</span></span>

<span data-ttu-id="03853-111">Der Outlook Connector für soziale Netzwerke (OSC) ruft **GetPeopleDetails** auf, wenn der osc-Anbieter die on-Demand-oder Hybrid Synchronisierung von Freunden und nicht-Freunden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="03853-111">The Outlook Social Connector (OSC) calls **GetPeopleDetails** if the OSC provider supports on-demand or hybrid synchronization of friends and non-friends.</span></span> 
  
<span data-ttu-id="03853-112">Der Parameter _personsAddresses_ muss der Schema Definition für **hashedAddresses**entsprechen, wie im Schema für osc-Anbieter Erweiterbarkeit definiert.</span><span class="sxs-lookup"><span data-stu-id="03853-112">The  _personsAddresses_ parameter must conform to the schema definition for **hashedAddresses**, as defined in the schema for OSC provider extensibility.</span></span> <span data-ttu-id="03853-113">Die _PERSONSADDRESSES_ -Zeichenfolge stellt einen Satz von Hash-SMTP-Adressen für jeden Benutzer dar, der im Personen Bereich angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="03853-113">The  _personsAddresses_ string represents a set of hashed SMTP addresses for each user displayed in the People Pane.</span></span> <span data-ttu-id="03853-114">Der Benutzer muss kein Freund des angemeldeten Benutzers sein, der durch die [ISocialSession:: LoggedOnUserName](isocialsession-loggedonusername.md) -Eigenschaft dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="03853-114">The user does not have to be a friend of the logged-on user represented by the [ISocialSession::LoggedOnUserName](isocialsession-loggedonusername.md) property.</span></span> <span data-ttu-id="03853-115">Die Hash-SMTP-Adressen werden mithilfe der Hashfunktion verschlüsselt, die durch das **hashFunction** -Element in den XML- **Funktionen** des Anbieters angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="03853-115">The hashed SMTP addresses are encrypted by using the hashing function specified by the **hashFunction** element in the provider's **capabilities** XML.</span></span> <span data-ttu-id="03853-116">OSC identifiziert jede **hashedAddress** in der _personAddresses_ -Auflistung mit einem **Index** -Element.</span><span class="sxs-lookup"><span data-stu-id="03853-116">The OSC identifies each **hashedAddress** in the  _personAddresses_ collection with an **index** element.</span></span> <span data-ttu-id="03853-117">Der Anbieter muss das **Index** -Element verwenden, um den XML \*\*\*\* -Code des Empfängers zu identifizieren, wenn er **Freundes** -XML für **GetPeopleDetails**zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="03853-117">The provider must use the **index** element to identify the recipient's **person** XML when it returns **friends** XML for **GetPeopleDetails**.</span></span> <span data-ttu-id="03853-118">Wenn der Empfänger kein registrierter Benutzer im sozialen Netzwerk ist, darf der Anbieter keinen **Personen** -XML-Code für diesen Empfänger zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="03853-118">If the recipient is not a registered user on the social network, the provider must not return any **person** XML for that recipient.</span></span> <span data-ttu-id="03853-119">Das **Index** -Element für jeden durch **Person** -XML dargestellten Netzwerkbenutzer entspricht dem **Index** -Element für den Empfänger in _personsAddresses_.</span><span class="sxs-lookup"><span data-stu-id="03853-119">The **index** element for each network user represented by **person** XML corresponds to the **index** element for the recipient in  _personsAddresses_.</span></span>
  
<span data-ttu-id="03853-120">OSC speichert die vom personencollection-Parameter __ zurückgegebenen Informationen im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="03853-120">The OSC stores the information returned by the  _personsCollection_ parameter in memory.</span></span> <span data-ttu-id="03853-121">Die __ XML-Zeichenfolge personencollection muss der Schema Definition für **Freunde**entsprechen, wie im Schema für osc-Anbieter Erweiterbarkeit definiert.</span><span class="sxs-lookup"><span data-stu-id="03853-121">The  _personsCollection_ XML string must conform to the schema definition for **friends**, as defined in the schema for OSC provider extensibility.</span></span> <span data-ttu-id="03853-122">Weitere Informationen dazu, wie der OSC diese Informationen im Arbeitsspeicher verwendet und aktualisiert, finden Sie unter [Synchronisieren von Freunden und Aktivitäten](synchronizing-friends-and-activities.md).</span><span class="sxs-lookup"><span data-stu-id="03853-122">For more information about how the OSC uses and updates this information in memory, see [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="03853-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="03853-123">See also</span></span>

- [<span data-ttu-id="03853-124">ISocialSession2 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="03853-124">ISocialSession2 : IUnknown</span></span>](isocialsession2iunknown.md)
- [<span data-ttu-id="03853-125">Synchronisieren von Freunden und Aktivitäten</span><span class="sxs-lookup"><span data-stu-id="03853-125">Synchronizing Friends and Activities</span></span>](synchronizing-friends-and-activities.md)

