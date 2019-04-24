---
title: Connect-Eigenschaft (RDS)
TOCTitle: Connect property (RDS)
ms:assetid: 11aa3284-18e9-6d2d-761b-c25090370b77
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248890(v=office.15)
ms:contentKeyID: 48543324
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 42e7dd643985cee9aef8887099eb90dcdb381f4e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295982"
---
# <a name="connect-property-rds"></a>Connect-Eigenschaft (RDS)

**Gilt für**: Access 2013, Office 2013

Gibt den Namen der Datenbank an, in der die Abfrage- und Aktualisierungsvorgänge ausgeführt werden.

Sie können die **Connect**-Eigenschaft zur Entwurfszeit in den OBJECT-Tags des [RDS.DataControl](datacontrol-object-rds.md)-Objekts bzw. zur Laufzeit im Skriptcode (z. B. VBScript) festlegen.

## <a name="syntax"></a>Syntax

Entwurfszeit: \<Parameter Name = "Connect" Wert = "ConnectionString"\>

Laufzeit: DataControl. Connect = "ConnectionString"

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*ConnectionString* |Eine gültige Verbindungszeichenfolge. Allgemeinere Informationen zu Verbindungszeichenfolgen finden Sie im Abschnitt zur [ConnectionString](connectionstring-property-ado.md)-Eigenschaft oder in der Dokumentation Ihres Anbieters.<br/><br/>**Hinweis**: Angeben von MS Remote als Anbieter für **RDS. DataControl** würde ein vierstufiges Szenario erstellen. Szenarien mit mehr als drei Ebenen wurden nicht getestet und sollten nicht erforderlich sein.|
|*DataControl* |Eine Objektvariable, die ein **RDS.DataControl**-Objekt darstellt.|

