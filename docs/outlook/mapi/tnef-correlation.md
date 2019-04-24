---
title: TNEF-Korrelation
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 93d1716d-a0be-45aa-85d2-6c9be65f5fd2
description: 'Letzte Änderung: 12. März 2013'
ms.openlocfilehash: 8d601bb2bbc65e21c5bc83179cc29e53ddd33876
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327398"
---
# <a name="tnef-correlation"></a><span data-ttu-id="1f9ff-103">TNEF-Korrelation</span><span class="sxs-lookup"><span data-stu-id="1f9ff-103">TNEF Correlation</span></span>

 
  
<span data-ttu-id="1f9ff-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1f9ff-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1f9ff-105">Einige Messagingsysteme führen eine Korrelations Prüfung für einen TNEF-Stream (Transport Neutral Encapsulation Format) aus, der an eine eingehende Nachricht angefügt ist, um zu überprüfen, ob der TNEF-Stream tatsächlich zu dieser Nachricht gehört.</span><span class="sxs-lookup"><span data-stu-id="1f9ff-105">Some messaging systems perform a correlation check on any Transport-Neutral Encapsulation Format (TNEF) stream attached to an inbound message to verify that the TNEF stream does in fact belong to that message.</span></span> <span data-ttu-id="1f9ff-106">Hierzu wird der Wert eines Felds in der Kopfzeile der eingehenden Nachricht mit einer Kopie dieses Werts abgeglichen, die in einer Eigenschaft im TNEF-Stream gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="1f9ff-106">This involves matching the value of some field in the header of the inbound message with a copy of that value stored in some property in the TNEF stream.</span></span> <span data-ttu-id="1f9ff-107">Werte, die vermutlich für jede Nachricht eindeutig sind, wie etwa Nachrichtennummern, werden normalerweise dafür verwendet.</span><span class="sxs-lookup"><span data-stu-id="1f9ff-107">Values that are presumably unique for each message, such as message ID numbers, are typically used for this.</span></span> <span data-ttu-id="1f9ff-108">Der Transport oder das Gateway, mit dem der TNEF-Stream erstellt wurde, ist dafür verantwortlich, einen geeigneten Wert aus dem Nachrichtenkopf auszuwählen und eine Kopie in einer entsprechenden Eigenschaft zu platzieren, bevor die Eigenschaften der ausgehenden Nachricht in den TNEF-Stream codiert werden.</span><span class="sxs-lookup"><span data-stu-id="1f9ff-108">The transport or gateway that created the TNEF stream is responsible for choosing an appropriate value from the message header and placing a copy into an appropriate property before encoding the outgoing message's properties into the TNEF stream.</span></span> <span data-ttu-id="1f9ff-109">Gateways oder Transports, die die Nachricht empfangen, können diese Eigenschaft dann aus dem TNEF-Stream extrahieren und sicherstellen, dass ihr Wert mit dem Wert des entsprechenden Kopfzeilenfelds in der eingehenden Nachricht übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="1f9ff-109">Gateways or transports that receive the message can then extract that property from the TNEF stream and verify that its value matches the value of the corresponding header field on the inbound message.</span></span>
  
<span data-ttu-id="1f9ff-110">Wenn die Werte nicht übereinstimmen, sollte das Gateway oder der Transport den TNEF-Datenstrom verwerfen und nur den systemeigenen Nachrichtenumschlag verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="1f9ff-110">If the values do not match, the gateway or transport should discard the TNEF stream and process only the native message envelope.</span></span> <span data-ttu-id="1f9ff-111">Solche Überprüfungen sind ratsam, da nicht-MAPI-basierte e-Mail-Clients möglicherweise eine Datei anfügen, die einen TNEF-Datenstrom aus einer alten Nachricht an eine Weiterleitung oder sogar eine nicht verbundene Nachricht enthält. Wenn dies nicht der Fall ist, kann ein solcher Fehler den Verlust des Nachrichtentexts verursachen.</span><span class="sxs-lookup"><span data-stu-id="1f9ff-111">Such checks are prudent because non-MAPI-based mail clients may attach a file that contains a TNEF stream from an old message to a forwarding or even an unrelated message; if not checked, such an error may cause the loss of message text.</span></span>
  
<span data-ttu-id="1f9ff-112">Der ausgewählte Header Feldwert muss für die Nachricht eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="1f9ff-112">The header field value chosen must be unique to the message.</span></span> <span data-ttu-id="1f9ff-113">Es gibt kein festes Kopfzeilenfeld für alle Messagingsysteme, da unterschiedliche Messagingsysteme unterschiedliche Kopfzeilenfelder verwenden, aber in der Regel weist das Messagingsystem der Nachricht, die für diesen Zweck geeignet ist, einen eindeutigen Bezeichner zu.</span><span class="sxs-lookup"><span data-stu-id="1f9ff-113">There is no fixed header field for all messaging systems because different messaging systems use different header fields, but typically the messaging system assigns a unique identifier to the message which is suitable for this purpose.</span></span> <span data-ttu-id="1f9ff-114">SMTP-Systeme verwenden beispielsweise in der Regel den MessageID-Header, während X. 400-Systeme normalerweise das IM_THIS_IPM-Attribut verwenden.</span><span class="sxs-lookup"><span data-stu-id="1f9ff-114">For example, SMTP systems typically use the MessageID header, while X.400 systems typically use the IM_THIS_IPM attribute.</span></span>
  

