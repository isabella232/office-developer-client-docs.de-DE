---
title: Senden von Nachrichtenübermittlungsberichten
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: abb12ec5-f0b7-488a-a75d-446f4be53e96
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 717494f30fd4d43e94a7c6a37770e2eab8ebb59e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593599"
---
# <a name="sending-message-delivery-reports"></a><span data-ttu-id="bfe24-103">Senden von Nachrichtenübermittlungsberichten</span><span class="sxs-lookup"><span data-stu-id="bfe24-103">Sending Message Delivery Reports</span></span>

  
  
<span data-ttu-id="bfe24-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bfe24-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bfe24-105">Einige zugrunde liegenden Messagingsysteme unterstützen Übermittlungsberichte und andere nicht.</span><span class="sxs-lookup"><span data-stu-id="bfe24-105">Some underlying messaging systems support delivery reports and some do not.</span></span> <span data-ttu-id="bfe24-106">Wie der Adressbuchhierarchie bestimmt, ob Clientanwendungen Nachricht Übermittlung oder Nondelivery-Berichte gesendet werden können, ist Implementierungsdetail einzelnen Transport-Anbieter.</span><span class="sxs-lookup"><span data-stu-id="bfe24-106">How the transport provider determines whether message delivery or nondelivery reports can be sent to client applications is an implementation detail specific to individual transport providers.</span></span> <span data-ttu-id="bfe24-107">Wenn Clientanwendungen Übermittlungsberichte gesendet werden können, mit Transportanbieter die [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) -Methode können um MAPI der erfolgreichen oder fehlgeschlagenen Lieferung für einen oder mehrere Empfänger zu informieren.</span><span class="sxs-lookup"><span data-stu-id="bfe24-107">If delivery reports can be sent to client applications, transport providers use the [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) method to notify MAPI of successful or unsuccessful delivery for one or more recipients.</span></span> <span data-ttu-id="bfe24-108">MAPI generiert Übermittlung oder Nondelivery Berichte an diesen Empfänger entspricht.</span><span class="sxs-lookup"><span data-stu-id="bfe24-108">MAPI then generates delivery or nondelivery reports corresponding to those recipients.</span></span> <span data-ttu-id="bfe24-109">Transportanbieter können auch eingehende Übermittlung und Nondelivery Berichte, die systemeigene Nachrichtensystem in MAPI-Übermittlung sind und Unzustellbarkeitsberichten über **StatusRecips**übersetzen.</span><span class="sxs-lookup"><span data-stu-id="bfe24-109">Transport providers can also translate incoming delivery and nondelivery reports that are native to the messaging system into MAPI delivery and nondelivery reports by means of **StatusRecips**.</span></span>
  

