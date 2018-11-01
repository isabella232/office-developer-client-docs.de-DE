---
title: Hinweise zur XML-Sicherheit
TOCTitle: XML Security Considerations
ms:assetid: ef2c7f59-f5a2-98d1-37c6-42cb35b26a40
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250214(v=office.15)
ms:contentKeyID: 48548575
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 69672b2993cb91ace5bd447b762f33fcbd66c1bc
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25868490"
---
# <a name="xml-security-considerations"></a>Hinweise zur XML-Sicherheit


**Betrifft**: Access 2013, Office 2013

## <a name="xml-security-considerations"></a>Überlegungen zur Sicherheit bei XML

Die Methoden **Save** und **Open** von ADO im **Recordset** -Objekt gelten für die Ausführung in Internet Explorer als nicht sicher. Wenn deshalb diese Methoden in Skriptcode verwendet werden, der in einer Anwendung oder einem Steuerelement ausgeführt wird, die bzw. das in einem Browser bereitgestellt wird, wirkt sich die Sicherheitskonfiguration des Browsers auf das Verhalten aus.

In Internet Explorer 5 gibt es standardmäßig in den Internetzonen Sicherheitseinschränkungen für solche Vorgänge. Mit dieser Konfiguration hat das **Recordset** -Objekt keinen Zugriff auf das lokale Datensystem auf dem Client sowie keinen Zugriff auf Datenquellen außerhalb der Domäne des Servers, von dem die Seite heruntergeladen wurde. Bei der Ausführung im Browserhost kann ein **Recordset** -Objekt nur in einer Datei gespeichert werden, wenn es sich auf dem Server befindet, von dem die Seite heruntergeladen wurde. Entsprechend können Sie ein **Recordset** -Objekt nur öffnen, indem Sie es aus einer Datei laden, wenn sich diese Datei auf dem Server befindet, von dem die Seite heruntergeladen wurde.

Weitere Informationen zur Sicherheit in Internet Explorer finden Sie im technischen Artikel "ADO and RDS Security Issues in Microsoft Internet Explorer" (in englischer Sprache).

