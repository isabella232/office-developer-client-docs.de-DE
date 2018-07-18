---
title: Festlegen der Transportreihenfolge
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4a140ec3-9520-4119-a975-0fb6c1049967
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 71d7ebf2bc8c7bbf3b5ee6ce60959fdeee79abe3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795518"
---
# <a name="setting-transport-order"></a><span data-ttu-id="580f3-103">Festlegen der Transportreihenfolge</span><span class="sxs-lookup"><span data-stu-id="580f3-103">Setting Transport Order</span></span>

  
  
<span data-ttu-id="580f3-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="580f3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="580f3-105">Die MAPI-Warteschlange weist die Verantwortung für ausgehende Nachrichten basierend auf der Adresstypen und Bezeichner, die Transportanbieter deklarieren, dass sie verarbeiten können.</span><span class="sxs-lookup"><span data-stu-id="580f3-105">The MAPI spooler assigns responsibility for outgoing messages based on the address types and identifiers that transport providers declare they can handle.</span></span> <span data-ttu-id="580f3-106">Transportanbieter veröffentlichen Sie eine Liste der unterstützten Adresstypen und Bezeichner – gespeichert in **MAPIUID** Strukturen – Wenn MAPI ihre [IXPLogon::AddressTypes](ixplogon-addresstypes.md) -Methode aufruft, direkt nach der Anmeldung.</span><span class="sxs-lookup"><span data-stu-id="580f3-106">Transport providers publish a list of supported address types and identifiers — stored in **MAPIUID** structures — when MAPI calls their [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method, directly after logon.</span></span> <span data-ttu-id="580f3-107">Typ der Adresse des Empfängers wird in seiner **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))-Eigenschaft gespeichert.</span><span class="sxs-lookup"><span data-stu-id="580f3-107">A recipient's address type is stored in its **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="580f3-108">Registrieren Sie sich für einen Adresstyp gibt an, MAPI, dass der Adressbuchhierarchie mit ihrer **PR_ADDRTYPE** -Eigenschaft, um den registrierten Adresstyp an Empfänger senden kann.</span><span class="sxs-lookup"><span data-stu-id="580f3-108">Registering for an address type indicates to MAPI that the transport provider can deliver to recipients with their **PR_ADDRTYPE** property set to the registered address type.</span></span> <span data-ttu-id="580f3-109">Registrieren für eine **MAPIUID** gibt entsprechend an, dass der Adressbuchhierarchie an Empfänger übermitteln kann, die von Eintragsbezeichner mit der registrierten **MAPIUID**dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="580f3-109">Similarly, registering for a **MAPIUID** indicates that the transport provider can deliver to recipients that are represented by entry identifiers with the registered **MAPIUID**.</span></span>
  
<span data-ttu-id="580f3-110">Die meisten Transportanbieter registrieren Sie sich für eine oder mehrere Adresstypen; wenige registrieren, indem Sie **MAPIUID**.</span><span class="sxs-lookup"><span data-stu-id="580f3-110">Most transport providers register for one or more address types; few register by **MAPIUID**.</span></span> <span data-ttu-id="580f3-111">Transport-Anbietern, die sind eng mit einer Adressbuchanbieter gekoppelt und Grundlegendes zu seinem Eintrags-ID-Format, können zur Verarbeitung von Nachrichten durch **MAPIUID**, wodurch die Leistung gesteigert registrieren.</span><span class="sxs-lookup"><span data-stu-id="580f3-111">Transport providers that are tightly coupled with an address book provider and understand its entry identifier format can register to handle messages by **MAPIUID**, thereby improving performance.</span></span> <span data-ttu-id="580f3-112">Diese Transportanbieter eng gekoppelten können die e-Mail-Adresse des Empfängers und andere erforderliche Informationen aus der Eintrags-ID ohne es mit einem Anruf **IMAPISupport::OpenEntry** öffnen extrahieren.</span><span class="sxs-lookup"><span data-stu-id="580f3-112">These tightly coupled transport providers can extract the recipient's email address and other necessary information from the entry identifier without having to open it with an **IMAPISupport::OpenEntry** call.</span></span> 
  
<span data-ttu-id="580f3-113">MAPI verwaltet einen Auftrag für Transportanbieter verwendet, wenn mehrere Transportanbieter für den gleichen Adresstyp oder **MAPIUID**registriert haben.</span><span class="sxs-lookup"><span data-stu-id="580f3-113">MAPI maintains an order for transport providers, used when multiple transport providers have registered for the same address type or **MAPIUID**.</span></span> <span data-ttu-id="580f3-114">Sie können diesen Auftrag außer Kraft setzen, durch Aufrufen von [IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md) und übergeben eine geordnete Liste von die s **MAPIUID**, der alle aktiven Transportanbieter auf den durch den Parameter _LpUIDList_ verwiesen.:</span><span class="sxs-lookup"><span data-stu-id="580f3-114">You can override this order by calling [IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md) and passing an ordered list of the **MAPIUID**s of all of the active transport providers pointed to by the  _lpUIDList_ parameter.:</span></span> 
  
<span data-ttu-id="580f3-115">Rufen Sie zum Abrufen einer Liste aller von einem Anbieter für die aktiven Transport behandelt werden können Adresstypen [IMAPISession::EnumAdrTypes](imapisession-enumadrtypes.md).</span><span class="sxs-lookup"><span data-stu-id="580f3-115">To retrieve a list of all of the address types that can be handled by one of the active transport providers, call [IMAPISession::EnumAdrTypes](imapisession-enumadrtypes.md).</span></span> <span data-ttu-id="580f3-116">**EnumAdrTypes** gibt ein Array von Zeichenfolgen, die beschreibt Adresstypen unterstützt der Transport-Anbieter, die in der aktuellen Sitzung aktiv sind.</span><span class="sxs-lookup"><span data-stu-id="580f3-116">**EnumAdrTypes** returns an array of strings that describes address types supported by the transport providers that are active in the current session.</span></span> 
  

