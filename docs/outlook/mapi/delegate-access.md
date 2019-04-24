---
title: Stellvertretungszugriff
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a863494f-0071-4d97-a6c4-26707ee00e04
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 3d6a0eaf8ad125a0ae1ea3abb57e2aa57e0bdfe3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336736"
---
# <a name="delegate-access"></a><span data-ttu-id="61a87-103">Stellvertretungszugriff</span><span class="sxs-lookup"><span data-stu-id="61a87-103">Delegate Access</span></span>

  
  
<span data-ttu-id="61a87-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="61a87-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="61a87-p101">Delegieren des Zugriffs bezieht sich auf die M�glichkeit des Benutzers als anderer Benutzer eine Nachricht senden oder Empfangen einer Nachricht an einen anderen Benutzer. Delegieren des Zugriffs ist ein Service Provider unabh�ngigen Feature von MAPI, das Transportanbieter unterst�tzt werden k�nnen, falls gew�nscht. Jedoch ist kein Anbieter dazu erforderlich. Delegieren des Zugriffs ist hilfreich, wenn es f�r einen Benutzer als Nachrichten senden oder Filtern eingehende Nachrichten auf, wenn ein Benutzer Nachrichtenspeicher eines anderen Benutzers zugreifen muss oder eines anderen Benutzers erforderlich ist. Bevor Sie eine Verbindung mit einem anderen Benutzerspeicher Stellvertretungsbenutzers zulassen, muss der Nachricht Speicheranbieter �berpr�fen, ob Stellvertretungsbenutzers die entsprechende Autorit�t verf�gt.</span><span class="sxs-lookup"><span data-stu-id="61a87-p101">Delegate access refers to the user's ability to send a message as another user or receive a message for another user. Delegate access is a service provider-independent feature of MAPI that transport providers can support if they choose. However, no provider is required to do so. Delegate access is valuable when it is necessary for a user to send messages as, or filter incoming messages for, another user or when a user must access another user's message store. Before allowing a delegate user to connect to another user's store, the message store provider must verify that the delegate user has the proper authority.</span></span> 
  
<span data-ttu-id="61a87-110">Es gibt zwei Gruppen von Eigenschaften, die zur Unterst�tzung von Zugriffsrechten f�r Stellvertretung verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="61a87-110">There are two groups of properties that are used to support delegate access:</span></span>
  
 <span data-ttu-id="61a87-111">**PR_SENT_REPRESENTING_ADDRTYPE** ([Pidtagsentrepresentingaddresstype (](pidtagsentrepresentingaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="61a87-111">**PR_SENT_REPRESENTING_ADDRTYPE** ([PidTagSentRepresentingAddressType](pidtagsentrepresentingaddresstype-canonical-property.md))</span></span> 
  
 <span data-ttu-id="61a87-112">**PR_SENT_REPRESENTING_EMAIL_ADDRESS** ([Pidtagsentrepresentingemailaddress (](pidtagsentrepresentingemailaddress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="61a87-112">**PR_SENT_REPRESENTING_EMAIL_ADDRESS** ([PidTagSentRepresentingEmailAddress](pidtagsentrepresentingemailaddress-canonical-property.md))</span></span> 
  
 <span data-ttu-id="61a87-113">**PR_SENT_REPRESENTING_ENTRYID** ([Pidtagsentrepresentingentryid (](pidtagsentrepresentingentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="61a87-113">**PR_SENT_REPRESENTING_ENTRYID** ([PidTagSentRepresentingEntryId](pidtagsentrepresentingentryid-canonical-property.md))</span></span> 
  
 <span data-ttu-id="61a87-114">**PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="61a87-114">**PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))</span></span> 
  
 <span data-ttu-id="61a87-115">**PR_SENT_REPRESENTING_SEARCH_KEY** ([Pidtagsentrepresentingsearchkey (](pidtagsentrepresentingsearchkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="61a87-115">**PR_SENT_REPRESENTING_SEARCH_KEY** ([PidTagSentRepresentingSearchKey](pidtagsentrepresentingsearchkey-canonical-property.md))</span></span> 
  
 <span data-ttu-id="61a87-116">**PR_RCVD_REPRESENTING_ADDRTYPE** ([Pidtagreceivedrepresentingaddresstype (](pidtagreceivedrepresentingaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="61a87-116">**PR_RCVD_REPRESENTING_ADDRTYPE** ([PidTagReceivedRepresentingAddressType](pidtagreceivedrepresentingaddresstype-canonical-property.md))</span></span> 
  
 <span data-ttu-id="61a87-117">**PR_RCVD_REPRESENTING_EMAIL_ADDRESS** ([Pidtagreceivedrepresentingemailaddress (](pidtagreceivedrepresentingemailaddress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="61a87-117">**PR_RCVD_REPRESENTING_EMAIL_ADDRESS** ([PidTagReceivedRepresentingEmailAddress](pidtagreceivedrepresentingemailaddress-canonical-property.md))</span></span> 
  
 <span data-ttu-id="61a87-118">**PR_RCVD_REPRESENTING_ENTRYID** ([PidTagReceivedRepresentingEntryId](pidtagreceivedrepresentingentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="61a87-118">**PR_RCVD_REPRESENTING_ENTRYID** ([PidTagReceivedRepresentingEntryId](pidtagreceivedrepresentingentryid-canonical-property.md))</span></span> 
  
 <span data-ttu-id="61a87-119">**PR_RCVD_REPRESENTING_NAME** ([PidTagReceivedRepresentingName](pidtagreceivedrepresentingname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="61a87-119">**PR_RCVD_REPRESENTING_NAME** ([PidTagReceivedRepresentingName](pidtagreceivedrepresentingname-canonical-property.md))</span></span> 
  
 <span data-ttu-id="61a87-120">**PR_RCVD_REPRESENTING_SEARCH_KEY** ([Pidtagreceivedrepresentingsearchkey (](pidtagreceivedrepresentingsearchkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="61a87-120">**PR_RCVD_REPRESENTING_SEARCH_KEY** ([PidTagReceivedRepresentingSearchKey](pidtagreceivedrepresentingsearchkey-canonical-property.md))</span></span> 
  
<span data-ttu-id="61a87-p102">F�r ausgehende Nachrichten den **PR_SENT_REPRESENTING** Eigenschaften identifiziert des messaging-Benutzers, der als Absender fungieren soll. Clients k�nnen diese Eigenschaften als Option festlegen. Wenn die **PR_SENT_REPRESENTING** Zeitpunkt nicht festgelegt werden des Anbieters Verantwortung zusammen mit den Eigenschaften **PR_SENDER** festgelegt ist, die Nachricht erreicht eine Adressbuchhierarchie Delegieren des Zugriffs, unterst�tzt.</span><span class="sxs-lookup"><span data-stu-id="61a87-p102">On outgoing messages, the **PR_SENT_REPRESENTING** properties identify the messaging user that should act as the sender. Clients can set these properties as an option. If the **PR_SENT_REPRESENTING** properties are not set by the time the message reaches a transport provider that supports delegate access, it is the provider's responsibility to set them along with the **PR_SENDER** properties.</span></span> 
  
<span data-ttu-id="61a87-p103">F�r eingehende Nachrichten identifizieren die **PR_RCVD_REPRESENTING** -Eigenschaften des Benutzers, der als Empf�nger fungieren soll. Zum �bermitteln von Delegatnachrichten Anbietern f�r die Daten�bertragung m�ssen die **PR_RCVD_REPRESENTING** und die **PR_RECEIVED_BY** Eigenschaften festlegen. Empfangen einer Nachricht Delegaten Clients sollten die Werte der Eigenschaften **PR_SENT_REPRESENTING** in die entsprechenden Eigenschaften **PR_RCVD_REPRESENTING** kopieren.</span><span class="sxs-lookup"><span data-stu-id="61a87-p103">On incoming messages, the **PR_RCVD_REPRESENTING** properties identify the user that should act as the recipient. Transport providers responsible for delivering delegate messages must set both the **PR_RCVD_REPRESENTING** and **PR_RECEIVED_BY** properties. Clients receiving a delegate message should copy the values of the **PR_SENT_REPRESENTING** properties to the corresponding **PR_RCVD_REPRESENTING** properties.</span></span> 
  
<span data-ttu-id="61a87-p104">Angenommen Sie, dass John Sallys Nachrichten erh�lt, w�hrend Sally im Urlaub ist. Die Eigenschaften **PR_RCVD_REPRESENTING** identifizieren John als Stellvertretung Empf�nger. Wenn John eine Antwort auf eine Nachricht, die er erhalten hat f�r Sally sendet, identifizieren Sie die Nachrichteneigenschaften **PR_SENDER** John als Absender. Da John Sally darstellt, von den Eigenschaften **PR_SENT_REPRESENTING** Sally identifiziert.</span><span class="sxs-lookup"><span data-stu-id="61a87-p104">For example, suppose John is receiving Sally's messages while Sally is on vacation. The **PR_RCVD_REPRESENTING** properties identify John as the delegate recipient. When John sends a reply to a message that he has received for Sally, the message's **PR_SENDER** properties identify John as the sender. Because John is representing Sally, the **PR_SENT_REPRESENTING** properties identify Sally.</span></span> 
  
<span data-ttu-id="61a87-p105">Transport-Anbieter f�r die Verarbeitung eingehender Delegatnachrichten in der Regel diese Nachrichten als der durch die Eigenschaften **PR_SENT_REPRESENTING** identifizierte messaging Benutzer und nicht als der durch die Eigenschaften **PR_SENDER** identifizierte Benutzer �bermitteln soll. Die Ausnahme zu dieser Regel ist, wenn es erforderlich ist, Berechtigungen und Transport Zugriffsarten �bereinstimmen. In diesem Fall kann eine Adressbuchhierarchie eine sendende Identit�t ausw�hlen.</span><span class="sxs-lookup"><span data-stu-id="61a87-p105">Transport providers handling incoming delegate messages should usually deliver these messages as the messaging user identified by the **PR_SENT_REPRESENTING** properties rather than as the user identified by the **PR_SENDER** properties. The exception to this rule is when it is necessary to match access privilege and transport types. In this case, a transport provider can choose a sending identity.</span></span> 
  
<span data-ttu-id="61a87-p106">Wenn die **PR_SENT_REPRESENTING** -Eigenschaften f�r eine eingehende Nachricht Stellvertretung nicht verf�gbar sind, muss der Adressbuchhierarchie �bermittlung behandeln, festgelegt, mit den Werten der entsprechenden **PR_SENDER** Eigenschaften. Wenn die **PR_SENT_REPRESENTING** Eigenschaften verf�gbar sind, aber der Adressbuchhierarchie keine Zugriffsrechte f�r Stellvertretung unterst�tzt, k�nnen sie die **PR_SENDER** -Eigenschaften f�r die �bermittlung verwenden.</span><span class="sxs-lookup"><span data-stu-id="61a87-p106">If the **PR_SENT_REPRESENTING** properties are unavailable for an incoming delegate message, the transport provider handling delivery must set them, using the values of the corresponding **PR_SENDER** properties. If the **PR_SENT_REPRESENTING** properties are available but the transport provider does not support delegate access, it can use the **PR_SENDER** properties for delivery.</span></span> 
  

