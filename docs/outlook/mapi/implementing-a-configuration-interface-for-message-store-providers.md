---
title: Implementieren einer Konfigurationsschnittstelle für Nachrichtenspeicheranbieter
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 508e6950-d483-4cbe-b817-8016f4aa5cd8
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: f7151841eef180a78a13ad161d197af783decfb4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792516"
---
# <a name="implementing-a-configuration-interface-for-message-store-providers"></a><span data-ttu-id="6dacc-103">Implementieren einer Konfigurationsschnittstelle für Nachrichtenspeicheranbieter</span><span class="sxs-lookup"><span data-stu-id="6dacc-103">Implementing a Configuration Interface for Message Store Providers</span></span>

  
  
<span data-ttu-id="6dacc-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6dacc-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6dacc-105">Nachricht-Anbieter werden benötigt, um eine Schnittstelle implementieren, die dem Benutzer ermöglicht, konfigurieren Sie den Nachricht Speicheranbieter auf dem Computer des Benutzers ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6dacc-105">Message store providers are required to implement an interface that allows the user to configure the message store provider to run on that user's computer.</span></span> <span data-ttu-id="6dacc-106">Der Nachricht Speicheranbieter wird normalerweise konfiguriert, wenn der Nachricht Speicheranbieter Profil eines Benutzers hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="6dacc-106">Typically, the message store provider is configured when the message store provider is added to a user's profile.</span></span> <span data-ttu-id="6dacc-107">Verarbeitet die Nachricht Speicheranbieter Konfiguration-Schnittstelle im allgemeinen Aufgaben wie das Festlegen von Benutzernamen und Kennwörter für geschützte Nachrichtenspeicher Pfade zu erforderlichen Dateien auswählen, und erstellen den zugrunde liegende Speichermechanismus wird verwendet, falls erforderlich.</span><span class="sxs-lookup"><span data-stu-id="6dacc-107">The message store provider's configuration interface generally handles tasks such as setting user names and passwords for protected message stores, choosing paths to necessary files, and creating the underlying storage mechanism it will use, if necessary.</span></span>
  
<span data-ttu-id="6dacc-108">Der Zugriff auf die Konfigurationsschnittstelle, die Sie implementieren erfolgt über zusätzliche Einstiegspunkte in Ihren Dienstanbieter Nachricht DLL-Datei.</span><span class="sxs-lookup"><span data-stu-id="6dacc-108">The configuration interface you implement is accessed through additional entry points in your message service provider's DLL.</span></span> <span data-ttu-id="6dacc-109">Weitere Informationen finden Sie unter [Konfigurieren eines Diensts Nachricht](configuring-a-message-service.md).</span><span class="sxs-lookup"><span data-stu-id="6dacc-109">For more information, see [Configuring a Message Service](configuring-a-message-service.md).</span></span> <span data-ttu-id="6dacc-110">Die Nachricht Speicheranbieter Konfigurationsschnittstelle ist die einzige Benutzeroberfläche, die eine Nachricht Speicheranbieter implementieren müssen.</span><span class="sxs-lookup"><span data-stu-id="6dacc-110">The message store provider's configuration interface is the only user interface that a message store provider must implement.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="6dacc-111">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6dacc-111">See also</span></span>



[<span data-ttu-id="6dacc-112">Nachrichtenspeicher-Features</span><span class="sxs-lookup"><span data-stu-id="6dacc-112">Message Store Features</span></span>](message-store-features.md)

