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
# <a name="mapping-of-internet-mail-attributes-to-mapi-properties"></a>Zuordnen von Internet-e-Mail-Attributen zu MAPI-Eigenschaften

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
In diesem Anhang wird beschrieben, wie ein MAPI-Transportanbieter oder ein MAPI-fähiges Gateway, das eine Verbindung mit dem Internet herstellt, zwischen MAPI-Nachrichteneigenschaften und SMTP-Nachrichtenattributen (Simple Mail Transport Protocol) übersetzen soll. SMTP ist das Messaging Protokoll, das in einem Großteil des Internets verwendet wird. SMTP definiert eine Gruppe von Nachrichtenkopfzeilen – den Nachrichtenumschlag und ein Nachrichteninhalts Format. SMTP ist vollständig in einem Satz von zwei Dokumenten dokumentiert, RFC 821 und RFC 822, die sich auf einer Reihe von FTP-und WWW-Standorten im Internet befinden.
  
Informationen zum SMTP-Protokoll, das für die Kommunikation mit SMTP-basierten e-Mail-Agents verwendet wird, finden Sie unter RFC 821, [https://www.rfc-editor.org](https://www.rfc-editor.org)"Simple Mail Transfer Protocol" unter.
  
Informationen zu Adressierungs-und Standardnachrichten Kopfzeilen finden Sie in [https://www.rfc-editor.org](https://www.rfc-editor.org)RFC 822, "Standard für das Format von ARPA-Internet Text Nachrichten" unter.
  
Für MIME lesen Sie RFC 1521, "MIME (Multipurpose Internet Mail Extensions), Teil 1: Mechanismen zum angeben und beschreiben des Formats von Internet Nachrichten Körpern" [https://www.rfc-editor.org](https://www.rfc-editor.org)unter.
  
Das Ziel der Zuordnung von SMTP-Nachrichtenattributen zu MAPI-Eigenschaften (und umgekehrt) besteht darin, sicherzustellen, dass der vollständige Inhalt der MAPI-Nachrichten, die über die systemeigenen SMTP-Nachrichtenattribute codiert werden können, zuverlässig zwischen verschiedenen MAPI-Daten austauschen kann. Komponenten, die über das Internet kommunizieren müssen. Dieses Dokument basiert auf der Arbeit, die bereits an solchen Komponenten bei Microsoft ausgeführt wurde. 
  
In diesem Dokument wird die Vertrautheit mit MAPI-Übertragungs-, TNEF-und SMTP-e-Mails vorausgesetzt. Sie strebt an, prägnant zu sein und nicht in einem klaren Licht.
  
Als Konvention bezieht sich "ausgehend" auf e-Mails, die von einem MAPI-kompatiblen UA oder MTA ins Internet Reisen, und "eingehend" bezieht sich auf e-Mails, die aus dem Internet in eine MAPI-Komponente Reisen.
  

