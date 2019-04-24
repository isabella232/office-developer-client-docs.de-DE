---
title: Übersicht über den MAPI-Transport Anbieter
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b193e819-749e-4642-8afc-dbc47b17b617
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 20b03f7c52ec86d1fb554bf69c53947c3dda4f36
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357344"
---
# <a name="mapi-transport-provider-overview"></a><span data-ttu-id="fd166-103">Übersicht über den MAPI-Transport Anbieter</span><span class="sxs-lookup"><span data-stu-id="fd166-103">MAPI Transport Provider Overview</span></span>

  
  
<span data-ttu-id="fd166-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fd166-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fd166-105">Transport Anbieter verarbeiten Nachrichtenübertragung und-Empfang und implementieren ggf. Sicherheit.</span><span class="sxs-lookup"><span data-stu-id="fd166-105">Transport providers handle message transmission and reception and implement security, if necessary.</span></span> <span data-ttu-id="fd166-106">Sie kümmern sich auch um alle erforderlichen Vorverarbeitungs-und Nachbearbeitungsaufgaben.</span><span class="sxs-lookup"><span data-stu-id="fd166-106">They also take care of any necessary preprocessing and postprocessing tasks.</span></span> <span data-ttu-id="fd166-107">Es gibt in der Regel einen Transportanbieter für jedes aktive Messagingsystem.</span><span class="sxs-lookup"><span data-stu-id="fd166-107">There is typically one transport provider for every active messaging system.</span></span>
  
<span data-ttu-id="fd166-108">Client Anwendungen kommunizieren mit dem Transportanbieter über einen Nachrichtenspeicher Anbieter.</span><span class="sxs-lookup"><span data-stu-id="fd166-108">Client applications communicate with the transport provider through a message store provider.</span></span> 
  
<span data-ttu-id="fd166-109">Transport Anbieter registrieren sich bei MAPI, um einen oder mehrere bestimmte Typen von Empfänger Einträgen zu behandeln.</span><span class="sxs-lookup"><span data-stu-id="fd166-109">Transport providers register with MAPI to handle one or more particular types of recipient entries.</span></span> <span data-ttu-id="fd166-110">Wenn eine Nachricht gesendet werden kann, muss MAPI bestimmen, welcher Transportanbieter die Übertragung verarbeiten soll.</span><span class="sxs-lookup"><span data-stu-id="fd166-110">When a message is ready to be sent, MAPI must determine which transport provider should handle the transmission.</span></span> <span data-ttu-id="fd166-111">Je nach Empfängertyp kann MAPI sogar mehrere Transportanbieter aufrufen.</span><span class="sxs-lookup"><span data-stu-id="fd166-111">Depending on the type of recipient, MAPI can even call upon more than one transport provider.</span></span> <span data-ttu-id="fd166-112">Wenn ein nicht verfügbarer Transportanbieter der einzige ist, der den Empfänger verarbeiten kann, wird die Nachrichtenübertragung verschoben, bis eine Verbindung mit diesem Anbieter hergestellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="fd166-112">If an unavailable transport provider is the only one that can handle the recipient, the message transmission will be postponed until a connection with that provider can be reestablished.</span></span>
  
<span data-ttu-id="fd166-113">Einige Messagingsysteme sind sichere Systeme; alle potenziellen Benutzer müssen eine Reihe gültiger Anmeldeinformationen eingeben, bevor der Zugriff zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="fd166-113">Some messaging systems are secure systems; all potential users are required to enter a set of valid credentials before access is permitted.</span></span> <span data-ttu-id="fd166-114">MAPI verhindert den unbefugten Zugriff auf solche Secure Messaging-Systeme, indem der Transportanbieter Anmeldeinformationen zur Anmeldezeit überprüfen kann.</span><span class="sxs-lookup"><span data-stu-id="fd166-114">MAPI prevents unauthorized access to such secure messaging systems by having the transport provider validate credentials at logon time.</span></span> 
  

