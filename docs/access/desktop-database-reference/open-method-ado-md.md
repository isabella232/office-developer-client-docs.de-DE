---
title: Open-Methode (ADO MD)
TOCTitle: Open method (ADO MD)
ms:assetid: 12395ff6-fe07-325a-2b69-007aa0b11ee6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248894(v=office.15)
ms:contentKeyID: 48543335
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 54f7ce4d5d588e644707cd7b466c29f619850824
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288399"
---
# <a name="open-method-ado-md"></a>Open-Methode (ADO MD)

**Gilt für**: Access 2013, Office 2013

Ruft die Ergebnisse einer multidimensionalen Abfrage ab, und gibt die Ergebnisse an eine Zellmenge zurück.

## <a name="syntax"></a>Syntax

*Cellset*. Open*Source*, *ActiveConnection*

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*Source* |Optional. Ein **Variant**-Wert, der eine gültige multidimensionale Abfrage ergibt, z. B. eine MDX-Abfrage (Multidimensional Expression). Das *Source*-Argument entspricht der [Source](source-property-ado-md.md)-Eigenschaft. Weitere Informationen zu MDX finden Sie in der Dokumentation zu OLE DB für OLAP im Microsoft Data Access Components SDK.|
|*ActiveConnection* |Optional. Ein **Variant**-Ausdruck, der eine Zeichenfolge ergibt, die entweder einen gültigen Namen einer ADO-[Connection](connection-object-ado.md)-Objektvariable oder eine Definition für eine Verbindung angibt. Das *ActiveConnection*-Argument gibt die Verbindung an, die verwendet werden soll, um das [Cellset](cellset-object-ado-md.md)-Objekt zu öffnen. Wenn Sie eine Verbindungsdefinition für dieses Argument weitergeben, öffnet ADO eine neue Verbindung mithilfe der angegebenen Parameter. Das *ActiveConnection*-Argument entspricht der [ActiveConnection](activeconnection-property-ado-md.md)-Eigenschaft.|

## <a name="remarks"></a>Bemerkungen

Die **Open**-Methode erzeugt einen Fehler, wenn einer der Parameter ausgelassen wird und vor dem Öffnen des **Cellset**-Objekts der entsprechende Eigenschaftswert nicht festgelegt wurde.

