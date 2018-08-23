---
title: Implementieren einer Konfigurationsschnittstelle für Nachrichtenspeicheranbieter
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 508e6950-d483-4cbe-b817-8016f4aa5cd8
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 15833768fbd148ae4e689b5a80ed3479823864cb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592927"
---
# <a name="implementing-a-configuration-interface-for-message-store-providers"></a><span data-ttu-id="4a30b-103">Implementieren einer Konfigurationsschnittstelle für Nachrichtenspeicheranbieter</span><span class="sxs-lookup"><span data-stu-id="4a30b-103">Implementing a Configuration Interface for Message Store Providers</span></span>

  
  
<span data-ttu-id="4a30b-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4a30b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4a30b-105">Nachricht-Anbieter werden benötigt, um eine Schnittstelle implementieren, die dem Benutzer ermöglicht, konfigurieren Sie den Nachricht Speicheranbieter auf dem Computer des Benutzers ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4a30b-105">Message store providers are required to implement an interface that allows the user to configure the message store provider to run on that user's computer.</span></span> <span data-ttu-id="4a30b-106">Der Nachricht Speicheranbieter wird normalerweise konfiguriert, wenn der Nachricht Speicheranbieter Profil eines Benutzers hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="4a30b-106">Typically, the message store provider is configured when the message store provider is added to a user's profile.</span></span> <span data-ttu-id="4a30b-107">Verarbeitet die Nachricht Speicheranbieter Konfiguration-Schnittstelle im allgemeinen Aufgaben wie das Festlegen von Benutzernamen und Kennwörter für geschützte Nachrichtenspeicher Pfade zu erforderlichen Dateien auswählen, und erstellen den zugrunde liegende Speichermechanismus wird verwendet, falls erforderlich.</span><span class="sxs-lookup"><span data-stu-id="4a30b-107">The message store provider's configuration interface generally handles tasks such as setting user names and passwords for protected message stores, choosing paths to necessary files, and creating the underlying storage mechanism it will use, if necessary.</span></span>
  
<span data-ttu-id="4a30b-108">Der Zugriff auf die Konfigurationsschnittstelle, die Sie implementieren erfolgt über zusätzliche Einstiegspunkte in Ihren Dienstanbieter Nachricht DLL-Datei.</span><span class="sxs-lookup"><span data-stu-id="4a30b-108">The configuration interface you implement is accessed through additional entry points in your message service provider's DLL.</span></span> <span data-ttu-id="4a30b-109">Weitere Informationen finden Sie unter [Konfigurieren eines Diensts Nachricht](configuring-a-message-service.md).</span><span class="sxs-lookup"><span data-stu-id="4a30b-109">For more information, see [Configuring a Message Service](configuring-a-message-service.md).</span></span> <span data-ttu-id="4a30b-110">Die Nachricht Speicheranbieter Konfigurationsschnittstelle ist die einzige Benutzeroberfläche, die eine Nachricht Speicheranbieter implementieren müssen.</span><span class="sxs-lookup"><span data-stu-id="4a30b-110">The message store provider's configuration interface is the only user interface that a message store provider must implement.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="4a30b-111">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4a30b-111">See also</span></span>



[<span data-ttu-id="4a30b-112">Nachrichtenspeicher-Features</span><span class="sxs-lookup"><span data-stu-id="4a30b-112">Message Store Features</span></span>](message-store-features.md)

