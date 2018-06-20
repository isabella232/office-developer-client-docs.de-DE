---
title: ISocialSession2GetPeopleDetails
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8733aab9-3a8e-4924-b62f-4e871d991c72
description: Gibt eine Zeichenfolge, die eine Auflistung von Person und Teile des Bildes Details für die durch den PersonsAddresses-Parameter angegebenen Benutzer enthält.
ms.openlocfilehash: 756f8de3a0615420826fe725528c92351d521832
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796000"
---
# <a name="isocialsession2getpeopledetails"></a><span data-ttu-id="7f714-103">ISocialSession2::GetPeopleDetails</span><span class="sxs-lookup"><span data-stu-id="7f714-103">ISocialSession2::GetPeopleDetails</span></span>

<span data-ttu-id="7f714-104">Gibt eine Zeichenfolge, die eine Auflistung von Person und Teile des Bildes Details für die durch den _PersonsAddresses_ -Parameter angegebenen Benutzer enthält.</span><span class="sxs-lookup"><span data-stu-id="7f714-104">Returns a string that contains a collection of person and picture details for the users specified by the  _personsAddresses_ parameter.</span></span> 
  
```cpp
HRESULT _stdcall GetPeopleDetails([in] BSTR personsAddresses, [out, retval] BSTR* personsCollection);
```

## <a name="parameters"></a><span data-ttu-id="7f714-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="7f714-105">Parameters</span></span>

<span data-ttu-id="7f714-106">_personsAddresses_</span><span class="sxs-lookup"><span data-stu-id="7f714-106">_personsAddresses_</span></span>
  
> <span data-ttu-id="7f714-107">[in] Ein XML-Zeichenfolge, die die Hash SMTP-Adressen einer Gruppe von Benutzern angibt.</span><span class="sxs-lookup"><span data-stu-id="7f714-107">[in] An XML string that specifies the hashed SMTP addresses of a set of users.</span></span>
    
<span data-ttu-id="7f714-108">_personsCollection_</span><span class="sxs-lookup"><span data-stu-id="7f714-108">_personsCollection_</span></span>
  
> <span data-ttu-id="7f714-109">[out] Eine XML-Zeichenfolge, die eine Auflistung von Person und Teile des Bildes Details enthält.</span><span class="sxs-lookup"><span data-stu-id="7f714-109">[out] An XML string that contains a collection of person and picture details.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7f714-110">Hinweise</span><span class="sxs-lookup"><span data-stu-id="7f714-110">Remarks</span></span>

<span data-ttu-id="7f714-111">Outlook Social Connector (OSC) **GetPeopleDetails** aufgerufen, wenn der OSC-Anbieter auf Abruf oder Hybriden Synchronisierung von Freunde und nicht Freunde unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7f714-111">The Outlook Social Connector (OSC) calls **GetPeopleDetails** if the OSC provider supports on-demand or hybrid synchronization of friends and non-friends.</span></span> 
  
<span data-ttu-id="7f714-112">Der Parameter _PersonsAddresses_ muss die Schemadefinition für **HashedAddresses**, gemäß Definition im Schema für die Erweiterbarkeit des OSC-Providers entsprechen.</span><span class="sxs-lookup"><span data-stu-id="7f714-112">The  _personsAddresses_ parameter must conform to the schema definition for **hashedAddresses**, as defined in the schema for OSC provider extensibility.</span></span> <span data-ttu-id="7f714-113">Die Zeichenfolge _PersonsAddresses_ stellt eine Reihe von Hash SMTP-Adressen für jeden Benutzer im Bereich Personen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="7f714-113">The  _personsAddresses_ string represents a set of hashed SMTP addresses for each user displayed in the People Pane.</span></span> <span data-ttu-id="7f714-114">Der Benutzer hat keinen Friend der angemeldete Benutzer von der [ISocialSession::LoggedOnUserName](isocialsession-loggedonusername.md) -Eigenschaft dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="7f714-114">The user does not have to be a friend of the logged-on user represented by the [ISocialSession::LoggedOnUserName](isocialsession-loggedonusername.md) property.</span></span> <span data-ttu-id="7f714-115">Hash SMTP-Adressen werden mithilfe der vom **HashFunction** -Element in der Anbieter **Funktionen** XML angegebenen Hashfunktion verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="7f714-115">The hashed SMTP addresses are encrypted by using the hashing function specified by the **hashFunction** element in the provider's **capabilities** XML.</span></span> <span data-ttu-id="7f714-116">Die OSC identifiziert jedes **HashedAddress** in der _PersonAddresses_ -Auflistung mit einem **Index** -Element.</span><span class="sxs-lookup"><span data-stu-id="7f714-116">The OSC identifies each **hashedAddress** in the  _personAddresses_ collection with an **index** element.</span></span> <span data-ttu-id="7f714-117">Der Anbieter muss das **Index** -Element zum Identifizieren des Empfängers **Person** XML bei Rückgabe **Freunde** XML für **GetPeopleDetails**verwenden.</span><span class="sxs-lookup"><span data-stu-id="7f714-117">The provider must use the **index** element to identify the recipient's **person** XML when it returns **friends** XML for **GetPeopleDetails**.</span></span> <span data-ttu-id="7f714-118">Wenn der Empfänger keinem registrierten Benutzer von dem sozialen Netzwerk ist, muss der Anbieter keine **Person** XML für diesen Empfänger zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="7f714-118">If the recipient is not a registered user on the social network, the provider must not return any **person** XML for that recipient.</span></span> <span data-ttu-id="7f714-119">Das **Index** -Element für jeden Netzwerkbenutzer von dargestellt durch **Person** XML entspricht dem **Index** -Element für den Empfänger in _PersonsAddresses_.</span><span class="sxs-lookup"><span data-stu-id="7f714-119">The **index** element for each network user represented by **person** XML corresponds to the **index** element for the recipient in  _personsAddresses_.</span></span>
  
<span data-ttu-id="7f714-120">Die OSC werden die Informationen zurückgegeben, die durch den Parameter _PersonsCollection_ im Arbeitsspeicher gespeichert.</span><span class="sxs-lookup"><span data-stu-id="7f714-120">The OSC stores the information returned by the  _personsCollection_ parameter in memory.</span></span> <span data-ttu-id="7f714-121">Die _PersonsCollection_ XML-Zeichenfolge muss der Schemadefinition für **Freunde**, gemäß Definition im Schema für die Erweiterbarkeit des OSC-Providers entsprechen.</span><span class="sxs-lookup"><span data-stu-id="7f714-121">The  _personsCollection_ XML string must conform to the schema definition for **friends**, as defined in the schema for OSC provider extensibility.</span></span> <span data-ttu-id="7f714-122">Weitere Informationen darüber, wie die OSC verwendet und diese Informationen im Speicher aktualisiert finden Sie unter [Synchronisieren Freunde und Aktivitäten](synchronizing-friends-and-activities.md).</span><span class="sxs-lookup"><span data-stu-id="7f714-122">For more information about how the OSC uses and updates this information in memory, see [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="7f714-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7f714-123">See also</span></span>

- [<span data-ttu-id="7f714-124">ISocialSession2: IUnknown</span><span class="sxs-lookup"><span data-stu-id="7f714-124">ISocialSession2 : IUnknown</span></span>](isocialsession2iunknown.md)
- [<span data-ttu-id="7f714-125">Synchronisieren von Freunde und Aktivitäten</span><span class="sxs-lookup"><span data-stu-id="7f714-125">Synchronizing Friends and Activities</span></span>](synchronizing-friends-and-activities.md)

