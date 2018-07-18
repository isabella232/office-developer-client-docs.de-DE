---
title: Senden von Nachrichtenübermittlungsberichten
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: abb12ec5-f0b7-488a-a75d-446f4be53e96
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: d94785df9becf46bbfad66465facea35202c6079
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795491"
---
# <a name="sending-message-delivery-reports"></a><span data-ttu-id="2c792-103">Senden von Nachrichtenübermittlungsberichten</span><span class="sxs-lookup"><span data-stu-id="2c792-103">Sending Message Delivery Reports</span></span>

  
  
<span data-ttu-id="2c792-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2c792-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2c792-105">Einige zugrunde liegenden Messagingsysteme unterstützen Übermittlungsberichte und andere nicht.</span><span class="sxs-lookup"><span data-stu-id="2c792-105">Some underlying messaging systems support delivery reports and some do not.</span></span> <span data-ttu-id="2c792-106">Wie der Adressbuchhierarchie bestimmt, ob Clientanwendungen Nachricht Übermittlung oder Nondelivery-Berichte gesendet werden können, ist Implementierungsdetail einzelnen Transport-Anbieter.</span><span class="sxs-lookup"><span data-stu-id="2c792-106">How the transport provider determines whether message delivery or nondelivery reports can be sent to client applications is an implementation detail specific to individual transport providers.</span></span> <span data-ttu-id="2c792-107">Wenn Clientanwendungen Übermittlungsberichte gesendet werden können, mit Transportanbieter die [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) -Methode können um MAPI der erfolgreichen oder fehlgeschlagenen Lieferung für einen oder mehrere Empfänger zu informieren.</span><span class="sxs-lookup"><span data-stu-id="2c792-107">If delivery reports can be sent to client applications, transport providers use the [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) method to notify MAPI of successful or unsuccessful delivery for one or more recipients.</span></span> <span data-ttu-id="2c792-108">MAPI generiert Übermittlung oder Nondelivery Berichte an diesen Empfänger entspricht.</span><span class="sxs-lookup"><span data-stu-id="2c792-108">MAPI then generates delivery or nondelivery reports corresponding to those recipients.</span></span> <span data-ttu-id="2c792-109">Transportanbieter können auch eingehende Übermittlung und Nondelivery Berichte, die systemeigene Nachrichtensystem in MAPI-Übermittlung sind und Unzustellbarkeitsberichten über **StatusRecips**übersetzen.</span><span class="sxs-lookup"><span data-stu-id="2c792-109">Transport providers can also translate incoming delivery and nondelivery reports that are native to the messaging system into MAPI delivery and nondelivery reports by means of **StatusRecips**.</span></span>
  

