---
title: Senden von nachrichtenÜbermittlungsBerichten
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: abb12ec5-f0b7-488a-a75d-446f4be53e96
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 2a31e7d088d5c1f94b272cb4d307f3aff99f32ee
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433080"
---
# <a name="sending-message-delivery-reports"></a><span data-ttu-id="c991c-103">Senden von nachrichtenÜbermittlungsBerichten</span><span class="sxs-lookup"><span data-stu-id="c991c-103">Sending Message Delivery Reports</span></span>

  
  
<span data-ttu-id="c991c-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c991c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c991c-105">Einige zugrunde liegende Messagingsysteme unterstützen Übermittlungsberichte und andere nicht.</span><span class="sxs-lookup"><span data-stu-id="c991c-105">Some underlying messaging systems support delivery reports and some do not.</span></span> <span data-ttu-id="c991c-106">Wie der Transportanbieter bestimmt, ob Nachrichtenübermittlungs-oder Unzustellbarkeitsberichte an Clientanwendungen gesendet werden können, ist ein Implementierungsdetail für einzelne Transportanbieter.</span><span class="sxs-lookup"><span data-stu-id="c991c-106">How the transport provider determines whether message delivery or nondelivery reports can be sent to client applications is an implementation detail specific to individual transport providers.</span></span> <span data-ttu-id="c991c-107">Wenn Übermittlungsberichte an Clientanwendungen gesendet werden können, verwenden Transportanbieter die [IMAPISupport:: StatusRecips](imapisupport-statusrecips.md) -Methode, um MAPI über eine erfolgreiche oder nicht erfolgreiche Übermittlung für einen oder mehrere Empfänger zu benachrichtigen.</span><span class="sxs-lookup"><span data-stu-id="c991c-107">If delivery reports can be sent to client applications, transport providers use the [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) method to notify MAPI of successful or unsuccessful delivery for one or more recipients.</span></span> <span data-ttu-id="c991c-108">MAPI generiert dann Zusteller-oder Unzustellbarkeitsberichte, die diesen Empfängern entsprechen.</span><span class="sxs-lookup"><span data-stu-id="c991c-108">MAPI then generates delivery or nondelivery reports corresponding to those recipients.</span></span> <span data-ttu-id="c991c-109">Transport Anbieter können auch eingehende und nicht zugestellte Berichte, die im Messagingsystem nativ sind, über **StatusRecips**in MAPI-Übermittlungs-und Unzustellbarkeitsberichte übersetzen.</span><span class="sxs-lookup"><span data-stu-id="c991c-109">Transport providers can also translate incoming delivery and nondelivery reports that are native to the messaging system into MAPI delivery and nondelivery reports by means of **StatusRecips**.</span></span>
  

