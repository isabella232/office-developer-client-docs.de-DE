---
title: Arten von Transport Anbietern
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 772ecab1-7e91-415b-bae8-af8ffb7b7ed9
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: ca224658552af105d95794b4dd01d2ac76fe084f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315379"
---
# <a name="types-of-transport-providers"></a><span data-ttu-id="8431a-103">Arten von Transport Anbietern</span><span class="sxs-lookup"><span data-stu-id="8431a-103">Types of Transport Providers</span></span>

  
  
<span data-ttu-id="8431a-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8431a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8431a-105">Alle Transportanbieter unterstützen eine Reihe von Standardfunktionen, wie zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="8431a-105">All transport providers support a range of standard features, such as:</span></span>
  
- <span data-ttu-id="8431a-106">Bereitstelleneiner ordnungsgemäßen Sicherheit für das zugrunde liegende Messagingsystem</span><span class="sxs-lookup"><span data-stu-id="8431a-106">Providing proper security for the underlying messaging system.</span></span>
    
- <span data-ttu-id="8431a-107">Senden und empfangen von Nachrichten vom zugrunde liegenden Messagingsystem.</span><span class="sxs-lookup"><span data-stu-id="8431a-107">Sending and receiving messages from the underlying messaging system.</span></span>
    
- <span data-ttu-id="8431a-108">Verfügbar machen der Adresstypen, die von den Transportanbietern unterstützt werden, damit die MAPI-Spooler-und Clientanwendungen Sie entsprechend verwenden können.</span><span class="sxs-lookup"><span data-stu-id="8431a-108">Exposing the address types the transport providers support so the MAPI spooler and client applications can use them appropriately.</span></span>
    
- <span data-ttu-id="8431a-109">Annehmen der Lieferung für bestimmte Empfänger.</span><span class="sxs-lookup"><span data-stu-id="8431a-109">Accepting delivery for specific recipients.</span></span>
    
<span data-ttu-id="8431a-110">Darüber hinaus unterstützt MAPI zwei spezielle Typen von Anbietern für bestimmte Messagingsysteme.</span><span class="sxs-lookup"><span data-stu-id="8431a-110">In addition, MAPI supports two specialized types of providers for specific messaging systems.</span></span>
  
|<span data-ttu-id="8431a-111">**Transporttyp**</span><span class="sxs-lookup"><span data-stu-id="8431a-111">**Transport type**</span></span>|<span data-ttu-id="8431a-112">**HinzugeFügte Funktionalität**</span><span class="sxs-lookup"><span data-stu-id="8431a-112">**Added functionality**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8431a-113">Remote Transport</span><span class="sxs-lookup"><span data-stu-id="8431a-113">Remote Transport</span></span>  <br/> |<span data-ttu-id="8431a-114">Ermöglicht die Interoperabilität mit Clients, die Remote verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="8431a-114">Enables interoperability with clients connected remotely.</span></span>  <br/> |
|<span data-ttu-id="8431a-115">TNEF-Transport</span><span class="sxs-lookup"><span data-stu-id="8431a-115">TNEF Transport</span></span>  <br/> |<span data-ttu-id="8431a-116">Ermöglicht die Bewahrung von MAPI-Eigenschaften auf Messagingsystemen, die Sie nicht unterstützen.</span><span class="sxs-lookup"><span data-stu-id="8431a-116">Allows MAPI properties to be preserved on messaging systems that do not support them.</span></span>  <br/> |
   
<span data-ttu-id="8431a-117">TNEF-Übertragungen werden zum Übersetzen von Nachrichten zwischen Messagingsystemen verwendet, die unterschiedliche MAPI-Eigenschaften unterstützen.</span><span class="sxs-lookup"><span data-stu-id="8431a-117">TNEF transports are used for translating messages between messaging systems that support different sets of MAPI properties.</span></span> <span data-ttu-id="8431a-118">TNEF-Übertragungen verwenden die MAPI- [ITnef: IUnknown](itnefiunknown.md) -Schnittstelle zum Konvertieren von Eigenschaften, die vom Zielsystem nicht direkt in einen binären Datenstrom, der an die Nachricht angefügt werden kann, dargestellt werden können.</span><span class="sxs-lookup"><span data-stu-id="8431a-118">TNEF transports use the MAPI [ITnef : IUnknown](itnefiunknown.md) interface to convert any properties that the destination system cannot represent directly into a binary data stream that can be attached to the message.</span></span> <span data-ttu-id="8431a-119">Später kann ein anderer TNEF-Transport **ITnef** verwenden, um den Datenstrom zu decodieren und die ursprünglichen MAPI-Eigenschaften für Clientanwendungen zur Verfügung zu stellen.</span><span class="sxs-lookup"><span data-stu-id="8431a-119">Later, another TNEF transport can use **ITnef** to decode the data stream and make the original MAPI properties available to client applications.</span></span> <span data-ttu-id="8431a-120">Darüber hinaus ist die TNEF-Unterstützung erforderlich, wenn der Transport benutzerdefinierte Nachrichtenklassen unterstützen muss.</span><span class="sxs-lookup"><span data-stu-id="8431a-120">Additionally, TNEF support is required if your transport needs to support custom message classes.</span></span> <span data-ttu-id="8431a-121">Weitere Informationen zum Implementieren von TNEF-Transporten finden Sie unter [Entwickeln eines TNEF-fähigen](developing-a-tnef-enabled-transport-provider.md)Transportanbieters.</span><span class="sxs-lookup"><span data-stu-id="8431a-121">For information about implementing TNEF transports, see [Developing a TNEF-Enabled Transport Provider](developing-a-tnef-enabled-transport-provider.md).</span></span>
  
<span data-ttu-id="8431a-122">Wenn es sich bei Ihrem Transportanbieter nicht um einen dieser Typen handelt, müssen Sie ihn mit den grundlegenden MAPI-Funktionen und Netzwerkfunktionen implementieren, die auf der Zielplattform zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="8431a-122">If your transport provider is not one of these types, you will have to implement it with the basic MAPI functions and networking functions available on your target platform.</span></span>
  

