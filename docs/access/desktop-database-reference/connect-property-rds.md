---
title: Verbinden-Eigenschaft (RDS)
TOCTitle: Connect property (RDS)
ms:assetid: 11aa3284-18e9-6d2d-761b-c25090370b77
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248890(v=office.15)
ms:contentKeyID: 48543324
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 49f62accab5a4da7d89c545bf82d0593238be1c2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59597618"
---
# <a name="connect-property-rds"></a>Verbinden-Eigenschaft (RDS)

**Gilt für**: Access 2013, Office 2013

Gibt den Namen der Datenbank an, in der die Abfrage- und Aktualisierungsvorgänge ausgeführt werden.

Sie können die **Connect**-Eigenschaft zur Entwurfszeit in den OBJECT-Tags des [RDS.DataControl](datacontrol-object-rds.md)-Objekts bzw. zur Laufzeit im Skriptcode (z. B. VBScript) festlegen.

## <a name="syntax"></a>Syntax

Entwurfszeit: \<PARAM NAME="Connect" VALUE="ConnectionString"\>

Laufzeit: DataControl. Verbinden = "ConnectionString"

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*ConnectionString* |Eine gültige Verbindungszeichenfolge. Allgemeinere Informationen zu Verbindungszeichenfolgen finden Sie im Abschnitt zur [ConnectionString](connectionstring-property-ado.md)-Eigenschaft oder in der Dokumentation Ihres Anbieters.<br/><br/>**HINWEIS:** Angeben von MS Remote als Anbieter für **rds. DataControl** würde ein vierstufiges Szenario erstellen. Szenarien mit mehr als drei Ebenen wurden nicht getestet und sollten nicht erforderlich sein.|
|*DataControl* |Eine Objektvariable, die ein **RDS.DataControl**-Objekt darstellt.|

