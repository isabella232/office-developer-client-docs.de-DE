---
title: LoadFromFile-Methode (ADO)
TOCTitle: LoadFromFile method (ADO)
ms:assetid: 33fd543f-bd24-9199-7540-2889b69221c8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249107(v=office.15)
ms:contentKeyID: 48544123
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c7b8492da87d0443d7992a1b9443501885ade3a0
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998581"
---
# <a name="loadfromfile-method-ado"></a>LoadFromFile-Methode (ADO)

**Betrifft**: Access 2013, Office 2013

Lädt den Inhalt einer vorhandenen Datei in ein [Stream](stream-object-ado.md)-Objekt.

## <a name="syntax"></a>Syntax

*Stream-Objekt*. LoadFromFile- *Dateiname*

## <a name="parameters"></a>Parameter

|Name |Beschreibung|
|:----|:----------|
|*FileName* |Ein **String** -Wert, der den Namen der in das **Stream** -Objekt zu ladenden Datei enthält. *FileName* kann auf einem beliebigen gültigen Pfad und Namen im UNC-Format enthalten. Wenn die angegebene Datei nicht vorhanden ist, tritt ein Laufzeitfehler auf.|

## <a name="remarks"></a>Hinweise

Diese Methode kann verwendet werden, um den Inhalt einer lokalen Datei in ein **Stream** -Objekt zu laden (z. B. zum Hochladen des Inhalts einer lokalen Datei auf einen Server).

Das **Stream** -Objekt muss vor dem Aufrufen von **LoadFromFile** bereits geöffnet sein. Diese Methode ändert die Bindung des **Stream** -Objekts nicht. Es bleibt an das Objekt gebunden, das durch die URL oder den **Record** angegeben wird, mit der bzw. dem das **Stream** -Objekt ursprünglich geöffnet wurde.

**LoadFromFile** überschreibt den aktuellen Inhalt des **Stream** -Objekts mit den aus der Datei gelesenen Daten. Alle im **Stream** -Objekt vorhandenen Bytes werden mit dem Inhalt der Datei überschrieben. Alle zuvor vorhandenen und verbleibenden Bytes, die auf das von [LoadFromFile](eos-property-ado.md) erstellte **EOS** folgen, werden abgeschnitten.

Nach einem Aufruf von LoadFromFile wird die aktuelle Position auf den Anfang des Stream-Objekts festgelegt (Position lautet 0).

Da dem Anfang des Datenstroms zur Verschlüsselung zwei Bytes hinzugefügt werden können, entspricht die Größe des Datenstroms möglicherweise nicht genau der Größe der Datei, aus der dieser geladen wurde.

