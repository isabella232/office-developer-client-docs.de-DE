---
title: Zuordnen von Internet-e-Mail-Attributen zu MAPI-Eigenschaften
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
# <a name="mapping-of-internet-mail-attributes-to-mapi-properties"></a><span data-ttu-id="8e8c0-103">Zuordnen von Internet-e-Mail-Attributen zu MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8e8c0-103">Mapping of Internet Mail Attributes to MAPI Properties</span></span>

  
  
<span data-ttu-id="8e8c0-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8e8c0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8e8c0-105">In diesem Anhang wird beschrieben, wie ein MAPI-Transportanbieter oder ein MAPI-fähiges Gateway, das eine Verbindung mit dem Internet herstellt, zwischen MAPI-Nachrichteneigenschaften und SMTP-Nachrichtenattributen (Simple Mail Transport Protocol) übersetzen soll.</span><span class="sxs-lookup"><span data-stu-id="8e8c0-105">This appendix describes how a MAPI transport provider or MAPI-aware gateway which connects to the Internet should translate between MAPI message properties and Simple Mail Transport Protocol (SMTP) message attributes.</span></span> <span data-ttu-id="8e8c0-106">SMTP ist das Messaging Protokoll, das in einem Großteil des Internets verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8e8c0-106">SMTP is the messaging protocol used on much of the Internet.</span></span> <span data-ttu-id="8e8c0-107">SMTP definiert eine Gruppe von Nachrichtenkopfzeilen – den Nachrichtenumschlag und ein Nachrichteninhalts Format.</span><span class="sxs-lookup"><span data-stu-id="8e8c0-107">SMTP defines a set of message headers — the message envelope — and a message content format.</span></span> <span data-ttu-id="8e8c0-108">SMTP ist vollständig in einem Satz von zwei Dokumenten dokumentiert, RFC 821 und RFC 822, die sich auf einer Reihe von FTP-und WWW-Standorten im Internet befinden.</span><span class="sxs-lookup"><span data-stu-id="8e8c0-108">SMTP is fully documented in a set of two documents, RFC 821 and RFC 822, which can be found at a number of FTP and WWW sites on the Internet.</span></span>
  
<span data-ttu-id="8e8c0-109">Informationen zum SMTP-Protokoll, das für die Kommunikation mit SMTP-basierten e-Mail-Agents verwendet wird, finden Sie unter RFC 821, [https://www.rfc-editor.org](https://www.rfc-editor.org)"Simple Mail Transfer Protocol" unter.</span><span class="sxs-lookup"><span data-stu-id="8e8c0-109">For information on the SMTP protocol used to communicate with SMTP-based mail agents, see RFC 821, "Simple Mail Transfer Protocol," at [https://www.rfc-editor.org](https://www.rfc-editor.org).</span></span>
  
<span data-ttu-id="8e8c0-110">Informationen zu Adressierungs-und Standardnachrichten Kopfzeilen finden Sie in [https://www.rfc-editor.org](https://www.rfc-editor.org)RFC 822, "Standard für das Format von ARPA-Internet Text Nachrichten" unter.</span><span class="sxs-lookup"><span data-stu-id="8e8c0-110">For addressing and standard message headers, see RFC 822, "Standard for the Format of ARPA Internet Text Messages," at [https://www.rfc-editor.org](https://www.rfc-editor.org).</span></span>
  
<span data-ttu-id="8e8c0-111">Für MIME lesen Sie RFC 1521, "MIME (Multipurpose Internet Mail Extensions), Teil 1: Mechanismen zum angeben und beschreiben des Formats von Internet Nachrichten Körpern" [https://www.rfc-editor.org](https://www.rfc-editor.org)unter.</span><span class="sxs-lookup"><span data-stu-id="8e8c0-111">For MIME, see RFC 1521, "MIME (Multipurpose Internet Mail Extensions) Part One: Mechanisms for Specifying and Describing the Format of Internet Message Bodies," at [https://www.rfc-editor.org](https://www.rfc-editor.org).</span></span>
  
<span data-ttu-id="8e8c0-112">Das Ziel der Zuordnung von SMTP-Nachrichtenattributen zu MAPI-Eigenschaften (und umgekehrt) besteht darin, sicherzustellen, dass der vollständige Inhalt der MAPI-Nachrichten, die über die systemeigenen SMTP-Nachrichtenattribute codiert werden können, zuverlässig zwischen verschiedenen MAPI-Daten austauschen kann. Komponenten, die über das Internet kommunizieren müssen.</span><span class="sxs-lookup"><span data-stu-id="8e8c0-112">The goal of mapping SMTP message attributes to MAPI properties (and vice versa) is to ensure that the full content of MAPI messages, over and above that which can be encoded using native SMTP message attributes, can be reliably exchanged among different MAPI components that must communicate over the Internet.</span></span> <span data-ttu-id="8e8c0-113">Dieses Dokument basiert auf der Arbeit, die bereits an solchen Komponenten bei Microsoft ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="8e8c0-113">This document is based on work already done on such components at Microsoft.</span></span> 
  
<span data-ttu-id="8e8c0-114">In diesem Dokument wird die Vertrautheit mit MAPI-Übertragungs-, TNEF-und SMTP-e-Mails vorausgesetzt.</span><span class="sxs-lookup"><span data-stu-id="8e8c0-114">This document assumes familiarity with MAPI transports, TNEF, and SMTP mail.</span></span> <span data-ttu-id="8e8c0-115">Sie strebt an, prägnant zu sein und nicht in einem klaren Licht.</span><span class="sxs-lookup"><span data-stu-id="8e8c0-115">It strives to be concise rather than abundantly clear.</span></span>
  
<span data-ttu-id="8e8c0-116">Als Konvention bezieht sich "ausgehend" auf e-Mails, die von einem MAPI-kompatiblen UA oder MTA ins Internet Reisen, und "eingehend" bezieht sich auf e-Mails, die aus dem Internet in eine MAPI-Komponente Reisen.</span><span class="sxs-lookup"><span data-stu-id="8e8c0-116">As a convention, "outbound" refers to mail traveling from a MAPI-compliant UA or MTA to the Internet, and "inbound" refers to mail traveling from the Internet to a MAPI component.</span></span>
  

