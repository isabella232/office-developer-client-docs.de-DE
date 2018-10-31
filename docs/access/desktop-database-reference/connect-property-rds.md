---
title: Connect-Eigenschaft (RDS)
TOCTitle: Connect Property (RDS)
ms:assetid: 11aa3284-18e9-6d2d-761b-c25090370b77
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248890(v=office.15)
ms:contentKeyID: 48543324
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 191ef13d4d3c73bfbee50d72720d7e450376dd23
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25862919"
---
# <a name="connect-property-rds"></a>Connect-Eigenschaft (RDS)


**Betrifft**: Access 2013 | Office 2013

Gibt den Namen der Datenbank an, in der die Abfrage- und Aktualisierungsvorgänge ausgeführt werden.

Sie können die **Connect** -Eigenschaft zur Entwurfszeit in den OBJECT-Tags des [RDS.DataControl](datacontrol-object-rds.md)-Objekts bzw. zur Laufzeit im Skriptcode (z. B. VBScript) festlegen.

## <a name="syntax"></a>Syntax

Entwurfszeit: \<PARAM NAME = "Verbinden" Wert = "ConnectionString"\>

Laufzeit: DataControl.Connect = "ConnectionString"

## <a name="parameters"></a>Parameter

- *ConnectionString*

  - Eine gültige Verbindungszeichenfolge. Allgemeinere Informationen zu Verbindungszeichenfolgen finden Sie im Abschnitt zur [ConnectionString](connectionstring-property-ado.md)-Eigenschaft oder in der Dokumentation Ihres Anbieters.
    
    > [!NOTE]
    > [!HINWEIS] Wenn Sie MS Remote als Anbieter für **RDS.DataControl** angeben, würde ein Szenario mit vier Ebenen erstellt. Szenarien mit mehr als drei Ebenen wurden nicht getestet und sollten nicht erforderlich sein.

- *DataControl*

  - Eine Objektvariable, die ein **RDS.DataControl**-Objekt darstellt.

