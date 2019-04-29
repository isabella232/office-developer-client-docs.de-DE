---
title: Festlegen des Transport Auftrags
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4a140ec3-9520-4119-a975-0fb6c1049967
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: efa2d6ab9edbd50634093b5185ef9036689f1379
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433598"
---
# <a name="setting-transport-order"></a><span data-ttu-id="058a5-103">Festlegen des Transport Auftrags</span><span class="sxs-lookup"><span data-stu-id="058a5-103">Setting Transport Order</span></span>

  
  
<span data-ttu-id="058a5-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="058a5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="058a5-105">Der MAPI-Spooler weist die Verantwortung für ausgehende Nachrichten auf Grundlage der Adresstypen und Bezeichner zu, die von den Transportanbietern deklariert werden können.</span><span class="sxs-lookup"><span data-stu-id="058a5-105">The MAPI spooler assigns responsibility for outgoing messages based on the address types and identifiers that transport providers declare they can handle.</span></span> <span data-ttu-id="058a5-106">Transport Anbieter veröffentlichen eine Liste unterstützter Adresstypen und Bezeichner, die in **MAPIUID** -Strukturen gespeichert sind, wenn MAPI Ihre [IXPLogon:: AddressTypes](ixplogon-addresstypes.md) -Methode direkt nach der Anmeldung aufruft.</span><span class="sxs-lookup"><span data-stu-id="058a5-106">Transport providers publish a list of supported address types and identifiers — stored in **MAPIUID** structures — when MAPI calls their [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method, directly after logon.</span></span> <span data-ttu-id="058a5-107">Der Adresstyp eines Empfängers wird in seiner **PR_ADDRTYPE** ([pidtagaddresstype (](pidtagaddresstype-canonical-property.md))-Eigenschaft gespeichert.</span><span class="sxs-lookup"><span data-stu-id="058a5-107">A recipient's address type is stored in its **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="058a5-108">Die Registrierung für einen Adresstyp gibt MAPI an, dass der Transportanbieter an Empfänger senden kann, deren **PR_ADDRTYPE** -Eigenschaft auf den registrierten Adresstyp festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="058a5-108">Registering for an address type indicates to MAPI that the transport provider can deliver to recipients with their **PR_ADDRTYPE** property set to the registered address type.</span></span> <span data-ttu-id="058a5-109">Entsprechend gibt die Registrierung für eine **MAPIUID** an, dass der Transportanbieter an Empfänger senden kann, die durch Eintrags-IDs mit der registrierten **MAPIUID**dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="058a5-109">Similarly, registering for a **MAPIUID** indicates that the transport provider can deliver to recipients that are represented by entry identifiers with the registered **MAPIUID**.</span></span>
  
<span data-ttu-id="058a5-110">Die meisten Transportanbieter registrieren für einen oder mehrere Adresstypen; wenige Register von **MAPIUID**.</span><span class="sxs-lookup"><span data-stu-id="058a5-110">Most transport providers register for one or more address types; few register by **MAPIUID**.</span></span> <span data-ttu-id="058a5-111">Transport Anbieter, die eng mit einem Adressbuchanbieter verbunden sind und dessen Eintrags-ID-Format verstehen, können sich registrieren, um Nachrichten von **MAPIUID**zu verarbeiten und dadurch die Leistung zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="058a5-111">Transport providers that are tightly coupled with an address book provider and understand its entry identifier format can register to handle messages by **MAPIUID**, thereby improving performance.</span></span> <span data-ttu-id="058a5-112">Diese eng gekoppelten Transportanbieter können die e-Mail-Adresse des Empfängers und andere erforderliche Informationen aus der Eintrags-ID extrahieren, ohne Sie mit einem **IMAPISupport:: OpenEntry** -Aufruf öffnen zu müssen.</span><span class="sxs-lookup"><span data-stu-id="058a5-112">These tightly coupled transport providers can extract the recipient's email address and other necessary information from the entry identifier without having to open it with an **IMAPISupport::OpenEntry** call.</span></span> 
  
<span data-ttu-id="058a5-113">MAPI verwaltet eine Bestellung für Transportanbieter, die verwendet wird, wenn mehrere Transportanbieter für denselben Adresstyp oder **MAPIUID**registriert haben.</span><span class="sxs-lookup"><span data-stu-id="058a5-113">MAPI maintains an order for transport providers, used when multiple transport providers have registered for the same address type or **MAPIUID**.</span></span> <span data-ttu-id="058a5-114">Sie können diese Reihenfolge überschreiben, indem Sie [IMsgServiceAdmin:: MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md) aufrufen und eine sortierte Liste der **MAPIUID**s aller aktiven Transportanbieter übergeben, auf die durch den _lpUIDList_ -Parameter verwiesen wird:</span><span class="sxs-lookup"><span data-stu-id="058a5-114">You can override this order by calling [IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md) and passing an ordered list of the **MAPIUID**s of all of the active transport providers pointed to by the  _lpUIDList_ parameter.:</span></span> 
  
<span data-ttu-id="058a5-115">Um eine Liste aller Adresstypen abzurufen, die von einem der aktiven Transportanbieter verarbeitet werden können, rufen Sie [IMAPISession:: EnumAdrTypes](imapisession-enumadrtypes.md)auf.</span><span class="sxs-lookup"><span data-stu-id="058a5-115">To retrieve a list of all of the address types that can be handled by one of the active transport providers, call [IMAPISession::EnumAdrTypes](imapisession-enumadrtypes.md).</span></span> <span data-ttu-id="058a5-116">**EnumAdrTypes** gibt ein Array von Zeichenfolgen zurück, in denen Adresstypen beschrieben werden, die von den Transportanbietern unterstützt werden, die in der aktuellen Sitzung aktiv sind.</span><span class="sxs-lookup"><span data-stu-id="058a5-116">**EnumAdrTypes** returns an array of strings that describes address types supported by the transport providers that are active in the current session.</span></span> 
  

