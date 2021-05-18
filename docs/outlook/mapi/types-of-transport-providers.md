---
title: Arten von Transportanbietern
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 772ecab1-7e91-415b-bae8-af8ffb7b7ed9
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: ca224658552af105d95794b4dd01d2ac76fe084f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406164"
---
# <a name="types-of-transport-providers"></a><span data-ttu-id="c74de-103">Arten von Transportanbietern</span><span class="sxs-lookup"><span data-stu-id="c74de-103">Types of Transport Providers</span></span>

  
  
<span data-ttu-id="c74de-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c74de-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c74de-105">Alle Transportanbieter unterstützen eine Reihe von Standardfeatures, z. B.:</span><span class="sxs-lookup"><span data-stu-id="c74de-105">All transport providers support a range of standard features, such as:</span></span>
  
- <span data-ttu-id="c74de-106">Bereitstellen der richtigen Sicherheit für das zugrunde liegende Messagingsystem.</span><span class="sxs-lookup"><span data-stu-id="c74de-106">Providing proper security for the underlying messaging system.</span></span>
    
- <span data-ttu-id="c74de-107">Senden und Empfangen von Nachrichten vom zugrunde liegenden Messagingsystem.</span><span class="sxs-lookup"><span data-stu-id="c74de-107">Sending and receiving messages from the underlying messaging system.</span></span>
    
- <span data-ttu-id="c74de-108">Das Verfügbar machen der Adresstypen, die von den Transportanbietern unterstützt werden, damit der MAPI-Spooler und Clientanwendungen sie entsprechend verwenden können.</span><span class="sxs-lookup"><span data-stu-id="c74de-108">Exposing the address types the transport providers support so the MAPI spooler and client applications can use them appropriately.</span></span>
    
- <span data-ttu-id="c74de-109">Akzeptieren der Zustellung für bestimmte Empfänger.</span><span class="sxs-lookup"><span data-stu-id="c74de-109">Accepting delivery for specific recipients.</span></span>
    
<span data-ttu-id="c74de-110">Darüber hinaus unterstützt MAPI zwei spezielle Anbietertypen für bestimmte Messagingsysteme.</span><span class="sxs-lookup"><span data-stu-id="c74de-110">In addition, MAPI supports two specialized types of providers for specific messaging systems.</span></span>
  
|<span data-ttu-id="c74de-111">**Transporttyp**</span><span class="sxs-lookup"><span data-stu-id="c74de-111">**Transport type**</span></span>|<span data-ttu-id="c74de-112">**Funktionalität hinzugefügt**</span><span class="sxs-lookup"><span data-stu-id="c74de-112">**Added functionality**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c74de-113">Remote-Transport</span><span class="sxs-lookup"><span data-stu-id="c74de-113">Remote Transport</span></span>  <br/> |<span data-ttu-id="c74de-114">Ermöglicht die Interoperabilität mit Remoteclients.</span><span class="sxs-lookup"><span data-stu-id="c74de-114">Enables interoperability with clients connected remotely.</span></span>  <br/> |
|<span data-ttu-id="c74de-115">TNEF-Transport</span><span class="sxs-lookup"><span data-stu-id="c74de-115">TNEF Transport</span></span>  <br/> |<span data-ttu-id="c74de-116">Ermöglicht das Beibehalten von MAPI-Eigenschaften auf Messagingsystemen, die sie nicht unterstützen.</span><span class="sxs-lookup"><span data-stu-id="c74de-116">Allows MAPI properties to be preserved on messaging systems that do not support them.</span></span>  <br/> |
   
<span data-ttu-id="c74de-117">TNEF-Transporte werden zum Übersetzen von Nachrichten zwischen Messagingsystemen verwendet, die unterschiedliche Sätze von MAPI-Eigenschaften unterstützen.</span><span class="sxs-lookup"><span data-stu-id="c74de-117">TNEF transports are used for translating messages between messaging systems that support different sets of MAPI properties.</span></span> <span data-ttu-id="c74de-118">TNEF-Transporte verwenden die MAPI [ITnef : IUnknown-Schnittstelle,](itnefiunknown.md) um eigenschaften, die das Zielsystem nicht direkt darstellen kann, in einen binären Datenstrom zu konvertieren, der an die Nachricht angefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="c74de-118">TNEF transports use the MAPI [ITnef : IUnknown](itnefiunknown.md) interface to convert any properties that the destination system cannot represent directly into a binary data stream that can be attached to the message.</span></span> <span data-ttu-id="c74de-119">Später kann ein anderer TNEF-Transport **ITnef** verwenden, um den Datenstrom zu decodieren und die ursprünglichen MAPI-Eigenschaften clientanwendungen zur Verfügung zu stellen.</span><span class="sxs-lookup"><span data-stu-id="c74de-119">Later, another TNEF transport can use **ITnef** to decode the data stream and make the original MAPI properties available to client applications.</span></span> <span data-ttu-id="c74de-120">Darüber hinaus ist TNEF-Unterstützung erforderlich, wenn Ihr Transport benutzerdefinierte Nachrichtenklassen unterstützen muss.</span><span class="sxs-lookup"><span data-stu-id="c74de-120">Additionally, TNEF support is required if your transport needs to support custom message classes.</span></span> <span data-ttu-id="c74de-121">Informationen zum Implementieren von TNEF-Transporten finden Sie unter [Developing a TNEF-Enabled Transport Provider](developing-a-tnef-enabled-transport-provider.md).</span><span class="sxs-lookup"><span data-stu-id="c74de-121">For information about implementing TNEF transports, see [Developing a TNEF-Enabled Transport Provider](developing-a-tnef-enabled-transport-provider.md).</span></span>
  
<span data-ttu-id="c74de-122">Wenn Ihr Transportanbieter nicht einer dieser Typen ist, müssen Sie ihn mit den grundlegenden MAPI-Funktionen und Netzwerkfunktionen implementieren, die auf Ihrer Zielplattform verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="c74de-122">If your transport provider is not one of these types, you will have to implement it with the basic MAPI functions and networking functions available on your target platform.</span></span>
  

