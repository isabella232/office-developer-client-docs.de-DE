---
title: Zuordnen von Internet-Mail-Attributen zu MAPI-Eigenschaften
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 79d1d2ba-34fe-4851-918f-adbc69c20eee
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: c9f77ea7ba56e7c559cf9b4c41a2d6f4d742b866
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59604733"
---
# <a name="mapping-of-internet-mail-attributes-to-mapi-properties"></a>Zuordnen von Internet-Mail-Attributen zu MAPI-Eigenschaften

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
In diesem Anhang wird beschrieben, wie ein MAPI-Transportanbieter oder MAPI-fähiges Gateway, das eine Verbindung mit dem Internet herstellt, zwischen MAPI-Nachrichteneigenschaften und SMTP-Nachrichtenattributen (Simple Mail Transport Protocol) übersetzt werden soll. SMTP ist das Messagingprotokoll, das in einem Großteil des Internets verwendet wird. SMTP definiert eine Reihe von Nachrichtenkopfzeilen – den Nachrichtenumschlag – und ein Nachrichteninhaltsformat. SMTP ist vollständig in zwei Dokumenten, RFC 821 und RFC 822, dokumentiert, die auf einer Reihe von FTP- und WWW-Websites im Internet zu finden sind.
  
Informationen zum SMTP-Protokoll, das für die Kommunikation mit SMTP-basierten E-Mail-Agents verwendet wird, finden Sie unter RFC 821, "Simple Mail Transfer Protocol". [https://www.rfc-editor.org](https://www.rfc-editor.org)
  
Informationen zum Adressieren und Standardnachrichtenkopfzeilen finden Sie unter RFC 822, "Standard for the Format of ARPA Internet Text [https://www.rfc-editor.org](https://www.rfc-editor.org) Messages".
  
Informationen zu MIME finden Sie unter RFC 1521, "MIME (Multipurpose Internet Mail Extensions) Part One: Mechanisms for Specifying and Describing the Format of Internet Message Bodies". [https://www.rfc-editor.org](https://www.rfc-editor.org)
  
Das Ziel der Zuordnung von SMTP-Nachrichtenattributen zu MAPI-Eigenschaften (und umgekehrt) besteht darin, sicherzustellen, dass der vollständige Inhalt von MAPI-Nachrichten über den Inhalt hinaus, der mit systemeigenen SMTP-Nachrichtenattributen codiert werden kann, zuverlässig zwischen verschiedenen MAPI-Komponenten ausgetauscht werden kann, die über das Internet kommunizieren müssen. Dieses Dokument basiert auf der Arbeit, die bereits an diesen Komponenten bei Microsoft durchgeführt wurde. 
  
Dieses Dokument setzt Voraus vertraut mit MAPI-Transporten, TNEF und SMTP-E-Mails. Sie ist bestrebt, prägnant und nicht eindeutig zu sein.
  
Als Konvention bezieht sich "ausgehend" auf E-Mails, die von einem MAPI-kompatiblen UA oder MTA in das Internet übertragen werden, und "eingehend" bezieht sich auf E-Mails, die aus dem Internet zu einer MAPI-Komponente übertragen werden.
  

