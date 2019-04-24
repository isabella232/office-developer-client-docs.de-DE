---
title: �bersicht �ber die MAPI-Programmierung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 30ac637a-874f-4660-b5d0-d28d69486f64
description: 'Letzte Änderung: Montag, 25. Juni 2012'
ms.openlocfilehash: d69d15f0f635c81bea30401b3a6d6e3ccf620112
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328273"
---
# <a name="mapi-programming-overview"></a><span data-ttu-id="8429f-103">Übersicht über die MAPI-Programmierung</span><span class="sxs-lookup"><span data-stu-id="8429f-103">MAPI Programming Overview</span></span>

  
  
<span data-ttu-id="8429f-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8429f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8429f-p101">Diese Referenz für Microsoft Outlook Messaging API (MAPI) wurde für C- und C++-Entwickler mit unterschiedlichen Anforderungen und Erfahrungen im Hinblick auf Messaging geschrieben. Für Entwickler, die mit MAPI ihre Anwendung mit Messaging-Funktionen erweitern möchten, sind keine speziellen Kenntnisse erforderlich. Sie benötigen Erfahrung mit Messaging und COM (Component Object Model), um MAPI zum Erstellen (COM) MAPI verwenden, um umfangreiche Arbeitsgruppenanwendungen oder Treiber für spezielle Messaging-Systemdienste zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="8429f-p101">This Microsoft Outlook Messaging API (MAPI) Reference is written for C and C++ developers with a variety of needs and experience with messaging. For those developers who want to use MAPI to augment their applications that have messaging features, no specific prerequisite knowledge is required. You need a background in messaging and the Component Object Model (COM) to use MAPI to create full-scale workgroup applications or drivers for specialized messaging system services.</span></span>
  
<span data-ttu-id="8429f-108">Bevor Sie mit der Entwicklungsarbeit beginnen, sollten Sie die folgenden Informationen zur Verwendung von MAPI, zum Anmeldevorgang und dar�ber ber�cksichtigen, wie Profile und Nachrichtendienste erstellt und konfiguriert sind.</span><span class="sxs-lookup"><span data-stu-id="8429f-108">Before starting development work, you should consider the following information about how to use MAPI, the logon process, and how profiles and message services are created and configured.</span></span>
  
<span data-ttu-id="8429f-p102">Die Messaging Application Program Interface (MAPI) ist eine umfassende Sammlung von Funktionen, die Entwickler verwenden k�nnen, um E-Mail-f�hige Anwendungen zu erstellen. Die vollst�ndige Funktionsbibliothek wird als MAPI bezeichnet. MAPI erm�glicht die vollst�ndige Kontrolle �ber das Messaging-System auf dem Clientcomputer, das Erstellen und Verwalten von Nachrichten und die Verwaltung des Clientpostfachs, der Dienstanbieter usw.</span><span class="sxs-lookup"><span data-stu-id="8429f-p102">The Messaging Application Program Interface (MAPI) is an extensive set of functions that developers can use to create mail-enabled applications. The full function library is known as MAPI. MAPI enables complete control over the messaging system on the client computer, creation and management of messages, management of the client mailbox, service providers, and so on.</span></span>
  
> [!NOTE]
> <span data-ttu-id="8429f-112">[!HINWEIS] Die erweiterte MAPI ist identisch mit MAPI und wird in der MAPI-Dokumentation einfach als MAPI bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="8429f-112">Extended MAPI is the same as MAPI, and is simply referred to as MAPI in the MAPI documentation.</span></span> 
  
 <span data-ttu-id="8429f-113">**Einfache MAPI**</span><span class="sxs-lookup"><span data-stu-id="8429f-113">**Simple MAPI**</span></span>
  
<span data-ttu-id="8429f-114">Die einfache MAPI bietet eine Reihe von Funktionen, mit denen Sie eine grundlegende Stufe von Messaging-Funktionen zu auf Microsoft Windows basierenden Anwendungen hinzuf�gen k�nnen.</span><span class="sxs-lookup"><span data-stu-id="8429f-114">Simple MAPI provides a set of functions that enables you to add a basic level of messaging functionality to Microsoft Windows-based applications.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="8429f-p103">[!WICHTIG] Die MAPISendMail-Funktion der einfachen MAPI wird von Microsoft Outlook 2013 und Microsoft Outlook 2010 unterst�tzt. Andere Funktionen der einfachen MAPI sind in Windows veraltet.</span><span class="sxs-lookup"><span data-stu-id="8429f-p103">The Simple MAPI function MAPISendMail is supported by Microsoft Outlook 2013 and Microsoft Outlook 2010. Other Simple MAPI functions have been deprecated in Windows.</span></span> 
  

