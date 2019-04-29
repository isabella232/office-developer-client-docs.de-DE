---
title: Implementieren einer Konfigurationsschnittstelle für Nachrichtenspeicher Anbieter
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 508e6950-d483-4cbe-b817-8016f4aa5cd8
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: c349a03b0be465ed1262712372b6ee17a9812abd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415887"
---
# <a name="implementing-a-configuration-interface-for-message-store-providers"></a><span data-ttu-id="d37ad-103">Implementieren einer Konfigurationsschnittstelle für Nachrichtenspeicher Anbieter</span><span class="sxs-lookup"><span data-stu-id="d37ad-103">Implementing a Configuration Interface for Message Store Providers</span></span>

  
  
<span data-ttu-id="d37ad-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d37ad-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d37ad-105">Nachrichtenspeicher Anbieter müssen eine Schnittstelle implementieren, die es dem Benutzer ermöglicht, den Nachrichtenspeicher Anbieter so zu konfigurieren, dass er auf dem Computer des Benutzers ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d37ad-105">Message store providers are required to implement an interface that allows the user to configure the message store provider to run on that user's computer.</span></span> <span data-ttu-id="d37ad-106">In der Regel wird der Nachrichtenspeicher Anbieter konfiguriert, wenn der Nachrichtenspeicher Anbieter dem Benutzerprofil hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="d37ad-106">Typically, the message store provider is configured when the message store provider is added to a user's profile.</span></span> <span data-ttu-id="d37ad-107">Die Konfigurationsschnittstelle des Nachrichtenspeicher Anbieters verarbeitet in der Regelaufgaben wie das Festlegen von Benutzernamen und Kennwörtern für geschützte Nachrichtenspeicher, das Auswählen von Pfaden zu den erforderlichen Dateien und das Erstellen des zugrunde liegenden Speichermechanismus, der bei Bedarf verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d37ad-107">The message store provider's configuration interface generally handles tasks such as setting user names and passwords for protected message stores, choosing paths to necessary files, and creating the underlying storage mechanism it will use, if necessary.</span></span>
  
<span data-ttu-id="d37ad-108">Der Zugriff auf die Konfigurationsschnittstelle, die Sie implementieren, erfolgt über zusätzliche Einstiegspunkte in der DLL des Nachrichten Dienstanbieters.</span><span class="sxs-lookup"><span data-stu-id="d37ad-108">The configuration interface you implement is accessed through additional entry points in your message service provider's DLL.</span></span> <span data-ttu-id="d37ad-109">Weitere Informationen finden Sie unter [Konfigurieren eines Nachrichtendiensts](configuring-a-message-service.md).</span><span class="sxs-lookup"><span data-stu-id="d37ad-109">For more information, see [Configuring a Message Service](configuring-a-message-service.md).</span></span> <span data-ttu-id="d37ad-110">Die Konfigurationsschnittstelle des Nachrichtenspeicher Anbieters ist die einzige Benutzeroberfläche, die ein Nachrichtenspeicher Anbieter implementieren muss.</span><span class="sxs-lookup"><span data-stu-id="d37ad-110">The message store provider's configuration interface is the only user interface that a message store provider must implement.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d37ad-111">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d37ad-111">See also</span></span>



[<span data-ttu-id="d37ad-112">Nachrichtenspeicher-Features</span><span class="sxs-lookup"><span data-stu-id="d37ad-112">Message Store Features</span></span>](message-store-features.md)

