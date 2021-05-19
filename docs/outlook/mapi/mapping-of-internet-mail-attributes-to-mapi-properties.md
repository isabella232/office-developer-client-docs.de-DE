---
title: Zuordnung von Internet-Mail-Attributen zu MAPI-Eigenschaften
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 79d1d2ba-34fe-4851-918f-adbc69c20eee
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: c0a71cbd3b6cdbef091e75ade5d190369a4626a4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355818"
---
# <a name="mapping-of-internet-mail-attributes-to-mapi-properties"></a><span data-ttu-id="5f4c7-103">Zuordnung von Internet-Mail-Attributen zu MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5f4c7-103">Mapping of Internet Mail Attributes to MAPI Properties</span></span>

  
  
<span data-ttu-id="5f4c7-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5f4c7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5f4c7-105">In diesem Anhang wird beschrieben, wie ein MAPI-Transportanbieter oder EIN -MAPI-benachrichtigungsgateway, das eine Verbindung mit dem Internet herstellt, zwischen DENI-Nachrichteneigenschaften und SMTP-Nachrichtenattributen (Simple Mail Transport Protocol) übersetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="5f4c7-105">This appendix describes how a MAPI transport provider or MAPI-aware gateway which connects to the Internet should translate between MAPI message properties and Simple Mail Transport Protocol (SMTP) message attributes.</span></span> <span data-ttu-id="5f4c7-106">SMTP ist das Messagingprotokoll, das in einem großen Teil des Internets verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5f4c7-106">SMTP is the messaging protocol used on much of the Internet.</span></span> <span data-ttu-id="5f4c7-107">SMTP definiert eine Reihe von Nachrichtenkopfzeilen – den Nachrichtenumschlag – und ein Nachrichteninhaltsformat.</span><span class="sxs-lookup"><span data-stu-id="5f4c7-107">SMTP defines a set of message headers — the message envelope — and a message content format.</span></span> <span data-ttu-id="5f4c7-108">SMTP ist vollständig in zwei Dokumenten dokumentiert, RFC 821 und RFC 822, die auf einer Reihe von FTP- und WWW-Websites im Internet zu finden sind.</span><span class="sxs-lookup"><span data-stu-id="5f4c7-108">SMTP is fully documented in a set of two documents, RFC 821 and RFC 822, which can be found at a number of FTP and WWW sites on the Internet.</span></span>
  
<span data-ttu-id="5f4c7-109">Informationen zum SMTP-Protokoll, das für die Kommunikation mit SMTP-basierten E-Mail-Agents verwendet wird, finden Sie unter RFC 821, "Simple Mail Transfer Protocol", unter [https://www.rfc-editor.org](https://www.rfc-editor.org) .</span><span class="sxs-lookup"><span data-stu-id="5f4c7-109">For information on the SMTP protocol used to communicate with SMTP-based mail agents, see RFC 821, "Simple Mail Transfer Protocol," at [https://www.rfc-editor.org](https://www.rfc-editor.org).</span></span>
  
<span data-ttu-id="5f4c7-110">Informationen zu Adressierung und Standardnachrichtenkopfzeilen finden Sie unter RFC 822, "Standard for the Format of ARPA Internet Text Messages", unter [https://www.rfc-editor.org](https://www.rfc-editor.org) .</span><span class="sxs-lookup"><span data-stu-id="5f4c7-110">For addressing and standard message headers, see RFC 822, "Standard for the Format of ARPA Internet Text Messages," at [https://www.rfc-editor.org](https://www.rfc-editor.org).</span></span>
  
<span data-ttu-id="5f4c7-111">Mime finden Sie unter RFC 1521, "MIME (Multipurpose Internet Mail Extensions) Part One: Mechanisms for Specifying and Describing the Format of Internet Message Bodies", unter [https://www.rfc-editor.org](https://www.rfc-editor.org) .</span><span class="sxs-lookup"><span data-stu-id="5f4c7-111">For MIME, see RFC 1521, "MIME (Multipurpose Internet Mail Extensions) Part One: Mechanisms for Specifying and Describing the Format of Internet Message Bodies," at [https://www.rfc-editor.org](https://www.rfc-editor.org).</span></span>
  
<span data-ttu-id="5f4c7-112">Das Ziel der Zuordnung von SMTP-Nachrichtenattributen zu MAPI-Eigenschaften (und umgekehrt) besteht in der Sicherstellung, dass der vollständige Inhalt von MAPI-Nachrichten, der über den Inhalt hinaus, der mit systemeigenen SMTP-Nachrichtenattributen codiert werden kann, zuverlässig zwischen verschiedenen MAPI-Komponenten ausgetauscht werden kann, die über das Internet kommunizieren müssen.</span><span class="sxs-lookup"><span data-stu-id="5f4c7-112">The goal of mapping SMTP message attributes to MAPI properties (and vice versa) is to ensure that the full content of MAPI messages, over and above that which can be encoded using native SMTP message attributes, can be reliably exchanged among different MAPI components that must communicate over the Internet.</span></span> <span data-ttu-id="5f4c7-113">Dieses Dokument basiert auf der Arbeit, die bereits an solchen Komponenten bei Microsoft durchgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="5f4c7-113">This document is based on work already done on such components at Microsoft.</span></span> 
  
<span data-ttu-id="5f4c7-114">In diesem Dokument wird die Vertrautheit mit MAPI-Transporten, TNEF und SMTP-E-Mails vorausgesetzt.</span><span class="sxs-lookup"><span data-stu-id="5f4c7-114">This document assumes familiarity with MAPI transports, TNEF, and SMTP mail.</span></span> <span data-ttu-id="5f4c7-115">Sie ist bestrebt, prägnant und nicht überdünslich klar zu sein.</span><span class="sxs-lookup"><span data-stu-id="5f4c7-115">It strives to be concise rather than abundantly clear.</span></span>
  
<span data-ttu-id="5f4c7-116">Als Konvention bezieht sich "ausgehend" auf E-Mails, die von einem MAPI-kompatiblen UA oder MTA in das Internet reisen, und "eingehenden" auf E-Mails, die aus dem Internet zu einer MAPI-Komponente reisen.</span><span class="sxs-lookup"><span data-stu-id="5f4c7-116">As a convention, "outbound" refers to mail traveling from a MAPI-compliant UA or MTA to the Internet, and "inbound" refers to mail traveling from the Internet to a MAPI component.</span></span>
  

