---
title: Outlook Connector für soziale Netzwerke Provider-Schnittstellen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8f92b2c7-9f47-4c84-874b-fec1a2a5b555
description: Outlook Social Connector (OSC) ist ein Office-Feature von Office-Clientanwendungen gemeinsam genutzt werden, die eine Verbindung mit sozialen herstellt und damit Benutzer die Personen in ihren Netzwerken mit ihr in Verbindung bleiben können, ohne Office Business-Netzwerke.
ms.openlocfilehash: bc393f32e563bbbef70538ea00cd92cf7f96729c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796079"
---
# <a name="outlook-social-connector-provider-interfaces"></a><span data-ttu-id="67a43-103">Outlook Connector für soziale Netzwerke Provider-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="67a43-103">Outlook Social Connector provider interfaces</span></span>

<span data-ttu-id="67a43-104">Outlook Social Connector (OSC) ist ein Office-Feature von Office-Clientanwendungen gemeinsam genutzt werden, die eine Verbindung mit sozialen herstellt und damit Benutzer die Personen in ihren Netzwerken mit ihr in Verbindung bleiben können, ohne Office Business-Netzwerke.</span><span class="sxs-lookup"><span data-stu-id="67a43-104">The Outlook Social Connector (OSC) is an Office feature shared by Office client applications that connects to social and business networks so users can stay in touch with the people in their networks without leaving Office.</span></span> 
  
<span data-ttu-id="67a43-105">Ein OSC-Provider ist eine DLL-Datei, mit der die OSC für soziale Netzwerke Zugriff auf Daten in eine Möglichkeit, die unabhängig von den einzelnen sozialen Netzwerk-APIs kann, Component Object Model (COM).</span><span class="sxs-lookup"><span data-stu-id="67a43-105">An OSC provider is a Component Object Model (COM) DLL that allows the OSC to access social network data in a way that is independent of the APIs of each social network.</span></span> <span data-ttu-id="67a43-106">Die folgende Tabelle enthält die Schnittstellen in die Erweiterbarkeit des OSC-Providers.</span><span class="sxs-lookup"><span data-stu-id="67a43-106">The following table lists the interfaces in OSC provider extensibility.</span></span> <span data-ttu-id="67a43-107">Ein OSC-Anbieter muss vier der fünf Schnittstellen zur Kommunikation mit dem OSC implementieren: [ISocialPerson](isocialpersoniunknown.md), [ISocialProfile](isocialprofileisocialperson.md), [ISocialProvider](isocialprovideriunknown.md)und [ISocialSession](isocialsessioniunknown.md).</span><span class="sxs-lookup"><span data-stu-id="67a43-107">An OSC provider must implement four of the five interfaces to communicate with the OSC: [ISocialPerson](isocialpersoniunknown.md), [ISocialProfile](isocialprofileisocialperson.md), [ISocialProvider](isocialprovideriunknown.md), and [ISocialSession](isocialsessioniunknown.md).</span></span> <span data-ttu-id="67a43-108">Wenn der OSC-Anbieter Synchronisieren von Aktivitäten auf Abruf unterstützt oder Hybrid Synchronisierung von Freunden, Anmeldeinformationen Zwischenspeichern von und Anmelden bei Verwendung zwischengespeichert Anmeldeinformationen oder die Möglichkeit, führen eine Person, sollte der Anbieter [ISocialSession2 implementieren. ](isocialsession2iunknown.md)rascher.</span><span class="sxs-lookup"><span data-stu-id="67a43-108">If the OSC provider supports synchronizing activities, on-demand or hybrid synchronization of friends, caching logon credentials and logging on using cached credentials, or the ability to follow a person, the provider should implement [ISocialSession2](isocialsession2iunknown.md), as well.</span></span>
  
|<span data-ttu-id="67a43-109">**Name**</span><span class="sxs-lookup"><span data-stu-id="67a43-109">**Name**</span></span>|<span data-ttu-id="67a43-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="67a43-110">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="67a43-111">ISocialPerson</span><span class="sxs-lookup"><span data-stu-id="67a43-111">ISocialPerson</span></span>](isocialpersoniunknown.md) <br/> |<span data-ttu-id="67a43-112">Stellt eine Person im sozialen Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="67a43-112">Represents a person on the social network.</span></span>  <br/> |
|[<span data-ttu-id="67a43-113">ISocialProfile</span><span class="sxs-lookup"><span data-stu-id="67a43-113">ISocialProfile</span></span>](isocialprofileisocialperson.md) <br/> |<span data-ttu-id="67a43-114">Stellt die angemeldeten Benutzers.</span><span class="sxs-lookup"><span data-stu-id="67a43-114">Represents the logged-on user.</span></span>  <br/> |
|[<span data-ttu-id="67a43-115">ISocialProvider</span><span class="sxs-lookup"><span data-stu-id="67a43-115">ISocialProvider</span></span>](isocialprovideriunknown.md) <br/> |<span data-ttu-id="67a43-116">Stellt eine Instanz eines OSC-Anbieters.</span><span class="sxs-lookup"><span data-stu-id="67a43-116">Represents an instance of an OSC provider.</span></span>  <br/> |
|[<span data-ttu-id="67a43-117">ISocialSession</span><span class="sxs-lookup"><span data-stu-id="67a43-117">ISocialSession</span></span>](isocialsessioniunknown.md) <br/> |<span data-ttu-id="67a43-118">Stellt eine Verbindung mit einer Website für soziale Netzwerke.</span><span class="sxs-lookup"><span data-stu-id="67a43-118">Represents a connection to a social network site.</span></span>  <br/> |
|[<span data-ttu-id="67a43-119">ISocialSession2</span><span class="sxs-lookup"><span data-stu-id="67a43-119">ISocialSession2</span></span>](isocialsession2iunknown.md) <br/> |<span data-ttu-id="67a43-120">Synchronisieren von Aktivitäten, Hinzufügen von Freunden unterstützt, zwischengespeicherten bei Bedarf oder Hybriden Synchronisierung von Freunde oder Anmelden bei der für soziale Netzwerke mithilfe von Anmeldeinformationen.</span><span class="sxs-lookup"><span data-stu-id="67a43-120">Supports synchronizing activities, adding friends, on-demand or hybrid synchronization of friends, or logging on to the social network by using cached credentials.</span></span>  <br/> |
   

