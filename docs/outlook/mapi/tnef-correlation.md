---
title: TNEF Korrelation
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 93d1716d-a0be-45aa-85d2-6c9be65f5fd2
description: 'Zuletzt geändert: 12 März 2013'
ms.openlocfilehash: b8b30dcc2fcf0c8e75004e36b6fd9f4f4583e304
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795737"
---
# <a name="tnef-correlation"></a><span data-ttu-id="2878a-103">TNEF Korrelation</span><span class="sxs-lookup"><span data-stu-id="2878a-103">TNEF Correlation</span></span>

 
  
<span data-ttu-id="2878a-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2878a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2878a-105">Einige Messagingsysteme führen Sie eine Überprüfung der Korrelation für jeden Transport-Neutral Encapsulation Format (TNEF) Stream, um sicherzustellen, dass der TNEF-Stream tatsächlich zu dieser Nachricht gehört eine eingehende Nachricht zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="2878a-105">Some messaging systems perform a correlation check on any Transport-Neutral Encapsulation Format (TNEF) stream attached to an inbound message to verify that the TNEF stream does in fact belong to that message.</span></span> <span data-ttu-id="2878a-106">Dieser Schritt umfasst das dem Wert der ein Feld in der Kopfzeile der eingehenden Nachricht mit einer Kopie des Werts in eine Eigenschaft in der TNEF-Stream gespeichert.</span><span class="sxs-lookup"><span data-stu-id="2878a-106">This involves matching the value of some field in the header of the inbound message with a copy of that value stored in some property in the TNEF stream.</span></span> <span data-ttu-id="2878a-107">Werte, die vermutlich eindeutig für jede Nachricht, wie etwa Nachricht-ID-Nummern sind werden in der Regel für diese verwendet.</span><span class="sxs-lookup"><span data-stu-id="2878a-107">Values that are presumably unique for each message, such as message ID numbers, are typically used for this.</span></span> <span data-ttu-id="2878a-108">Die Transport oder das Gateway, die den TNEF-Stream erstellt ist verantwortlich für einen entsprechenden Wert aus der Nachrichtenkopf auswählen und platziert eine Kopie in einer entsprechenden Eigenschaft vor die ausgehende Nachricht Eigenschaften in den Stream TNEF-Codierung.</span><span class="sxs-lookup"><span data-stu-id="2878a-108">The transport or gateway that created the TNEF stream is responsible for choosing an appropriate value from the message header and placing a copy into an appropriate property before encoding the outgoing message's properties into the TNEF stream.</span></span> <span data-ttu-id="2878a-109">Gateways oder Transporten, die die Nachricht empfangen können dann diese Eigenschaft aus dem TNEF-Stream extrahieren und stellen Sie sicher, dass der Wert den Wert des entsprechenden Felds Kopfzeile der eingehenden Nachricht übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="2878a-109">Gateways or transports that receive the message can then extract that property from the TNEF stream and verify that its value matches the value of the corresponding header field on the inbound message.</span></span>
  
<span data-ttu-id="2878a-110">Wenn die Werte nicht übereinstimmen, sollte das Gateway oder Transport die TNEF-Stream und Prozess nur die systemeigene Nachrichtenumschlag verwerfen.</span><span class="sxs-lookup"><span data-stu-id="2878a-110">If the values do not match, the gateway or transport should discard the TNEF stream and process only the native message envelope.</span></span> <span data-ttu-id="2878a-111">Kontrollen sind ratsam, da nicht-MAPI-basierten e-Mail-Clients können eine Datei anfügen, die einen TNEF-Stream aus einer alten Nachricht an eine Weiterleitung oder sogar eine unabhängige Nachricht enthält. Wenn nicht aktiviert, möglicherweise eine solche Fehlermeldung den Verlust des Nachrichtentexts.</span><span class="sxs-lookup"><span data-stu-id="2878a-111">Such checks are prudent because non-MAPI-based mail clients may attach a file that contains a TNEF stream from an old message to a forwarding or even an unrelated message; if not checked, such an error may cause the loss of message text.</span></span>
  
<span data-ttu-id="2878a-112">Der Wert des Felds Kopfzeile ausgewählt muss an die Nachricht eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="2878a-112">The header field value chosen must be unique to the message.</span></span> <span data-ttu-id="2878a-113">Keine festen Kopfzeilenfeld für alle Messagingsysteme vorhanden ist, da verschiedene Messagingsystemen unterschiedliche Kopf-Felder verwendet werden, aber in der Regel das messaging-System weist einen eindeutigen Bezeichner der Nachricht, die für diesen Zweck geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="2878a-113">There is no fixed header field for all messaging systems because different messaging systems use different header fields, but typically the messaging system assigns a unique identifier to the message which is suitable for this purpose.</span></span> <span data-ttu-id="2878a-114">Beispielsweise verwenden SMTP-Systeme in der Regel die Kopfzeile MessageID während x. 400-Systeme in der Regel das IM_THIS_IPM-Attribut verwenden.</span><span class="sxs-lookup"><span data-stu-id="2878a-114">For example, SMTP systems typically use the MessageID header, while X.400 systems typically use the IM_THIS_IPM attribute.</span></span>
  

