---
title: Zuordnung von Internet Mail-Attributen zu MAPI-Eigenschaften
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 79d1d2ba-34fe-4851-918f-adbc69c20eee
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 4d1bc5fc5a5e304d81ab4252a527d0e52b0d6e3c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793167"
---
# <a name="mapping-of-internet-mail-attributes-to-mapi-properties"></a><span data-ttu-id="eee23-103">Zuordnung von Internet Mail-Attributen zu MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="eee23-103">Mapping of Internet Mail Attributes to MAPI Properties</span></span>

  
  
<span data-ttu-id="eee23-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="eee23-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="eee23-105">In diesem Anhang wird beschrieben, wie ein MAPI-Transportdienst oder MAPI-fähigen Gateway mit dem Internet verbunden zwischen MAPI Nachrichteneigenschaften und Simple Mail Transport Protocol (SMTP) Nachrichtenattribute übersetzen sollten.</span><span class="sxs-lookup"><span data-stu-id="eee23-105">This appendix describes how a MAPI transport provider or MAPI-aware gateway which connects to the Internet should translate between MAPI message properties and Simple Mail Transport Protocol (SMTP) message attributes.</span></span> <span data-ttu-id="eee23-106">SMTP ist das messaging auf einen Großteil der im Internet verwendete Protokoll.</span><span class="sxs-lookup"><span data-stu-id="eee23-106">SMTP is the messaging protocol used on much of the Internet.</span></span> <span data-ttu-id="eee23-107">SMTP definiert eine Reihe von Nachrichtenkopfzeilen – der Nachrichtenumschlag – und einen Content-Nachrichtenformat.</span><span class="sxs-lookup"><span data-stu-id="eee23-107">SMTP defines a set of message headers — the message envelope — and a message content format.</span></span> <span data-ttu-id="eee23-108">SMTP ist vollständig dokumentiert, in einem Satz von zwei Dokumenten, RFC 821 und RFC 822 einer Reihe von FTP und WWW-Websites im Internet gefunden werden kann.</span><span class="sxs-lookup"><span data-stu-id="eee23-108">SMTP is fully documented in a set of two documents, RFC 821 and RFC 822, which can be found at a number of FTP and WWW sites on the Internet.</span></span>
  
<span data-ttu-id="eee23-109">Informationen über das SMTP-Protokoll verwendet, um eine Kommunikation mit SMTP-basierte e-Mail-Agenten, finden Sie in RFC 821 "Simple Mail Transfer Protocol," unter [http://www.rfc-editor.org](http://www.rfc-editor.org).</span><span class="sxs-lookup"><span data-stu-id="eee23-109">For information on the SMTP protocol used to communicate with SMTP-based mail agents, see RFC 821, "Simple Mail Transfer Protocol," at [http://www.rfc-editor.org](http://www.rfc-editor.org).</span></span>
  
<span data-ttu-id="eee23-110">Reagieren auf und standard Nachrichtenkopfzeilen finden Sie im RFC 822, "Standard für das Format von ARPA Internet-Textnachrichten," unter [http://www.rfc-editor.org](http://www.rfc-editor.org).</span><span class="sxs-lookup"><span data-stu-id="eee23-110">For addressing and standard message headers, see RFC 822, "Standard for the Format of ARPA Internet Text Messages," at [http://www.rfc-editor.org](http://www.rfc-editor.org).</span></span>
  
<span data-ttu-id="eee23-111">MIME, finden Sie unter RFC 1521, "MIME (Multipurpose Internet Mail Extensions)-Teil einer: Mechanismen zum angeben und Beschreiben des Formats Internet Message Bodies" unter [http://www.rfc-editor.org](http://www.rfc-editor.org).</span><span class="sxs-lookup"><span data-stu-id="eee23-111">For MIME, see RFC 1521, "MIME (Multipurpose Internet Mail Extensions) Part One: Mechanisms for Specifying and Describing the Format of Internet Message Bodies," at [http://www.rfc-editor.org](http://www.rfc-editor.org).</span></span>
  
<span data-ttu-id="eee23-112">Das Ziel der Zuordnung SMTP Nachrichtenattribute zu MAPI-Eigenschaften (und umgekehrt) ist, stellen Sie sicher, dass des gesamten Inhalts der MAPI-Nachrichten über die mit systemeigenen SMTP-Nachrichtenattribute codiert werden können, zwischen verschiedenen MAPI zuverlässig ausgetauscht werden können Komponenten, die über das Internet kommunizieren müssen.</span><span class="sxs-lookup"><span data-stu-id="eee23-112">The goal of mapping SMTP message attributes to MAPI properties (and vice versa) is to ensure that the full content of MAPI messages, over and above that which can be encoded using native SMTP message attributes, can be reliably exchanged among different MAPI components that must communicate over the Internet.</span></span> <span data-ttu-id="eee23-113">Dieses Dokument basiert auf arbeiten, die bereits an eine solche Komponenten bei Microsoft.</span><span class="sxs-lookup"><span data-stu-id="eee23-113">This document is based on work already done on such components at Microsoft.</span></span> 
  
<span data-ttu-id="eee23-114">In diesem Dokument wird davon ausgegangen, gute Kenntnisse im Umgang mit MAPI-Transport, TNEF und SMTP-Mail.</span><span class="sxs-lookup"><span data-stu-id="eee23-114">This document assumes familiarity with MAPI transports, TNEF, and SMTP mail.</span></span> <span data-ttu-id="eee23-115">Es ist bestrebt, Risiken löschen, statt präzise sein.</span><span class="sxs-lookup"><span data-stu-id="eee23-115">It strives to be concise rather than abundantly clear.</span></span>
  
<span data-ttu-id="eee23-116">Als eine Konvention "Ausgehend" verweist auf Reisen aus einem MAPI-kompatible UA oder MTA mit dem Internet mail und "eingehenden" bezieht sich auf Reisen über das Internet zu einer Komponente MAPI Mail.</span><span class="sxs-lookup"><span data-stu-id="eee23-116">As a convention, "outbound" refers to mail traveling from a MAPI-compliant UA or MTA to the Internet, and "inbound" refers to mail traveling from the Internet to a MAPI component.</span></span>
  

