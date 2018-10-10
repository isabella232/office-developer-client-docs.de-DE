---
title: Open-Methode (ADO MD)
TOCTitle: Open Method (ADO MD)
ms:assetid: 12395ff6-fe07-325a-2b69-007aa0b11ee6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248894(v=office.15)
ms:contentKeyID: 48543335
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ad4d1c05637f2ff7ef5ff65ec26ab1b721495067
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25472645"
---
# <a name="open-method-ado-md"></a>Open-Methode (ADO MD)


**Betrifft**: Access 2013 | Office 2013

Ruft die Ergebnisse einer multidimensionalen Abfrage ab, und gibt die Ergebnisse an eine Zellmenge zurück.

## <a name="syntax"></a>Syntax

*Zellmenge*. Open-*Source*, *ActiveConnection*

## <a name="parameters"></a>Parameter

  - *Source*

  - Optional. Ein **Variant-Wert** , der eine gültige multidimensionale Abfrage, beispielsweise eine Abfrage (Multidimensional Expression) ausgewertet wird. Das Argument *Source* entspricht die [Source](source-property-ado-md.md) -Eigenschaft. Weitere Informationen zu MDX finden Sie unter OLE DB für OLAP-Dokumentation, die in der Microsoft Data Access Components SDK.

  - *ActiveConnection*

  - Optional. Ein **Variant** -Ausdruck, der eine Zeichenfolge ergibt, die entweder einen gültigen Namen einer ADO- [Connection](connection-object-ado.md)-Objektvariable oder eine Definition für eine Verbindung angibt. Das *ActiveConnection* -Argument gibt die Verbindung an, die zum Öffnen des [Cellset](cellset-object-ado-md.md) -Objekts an. Wenn Sie eine Verbindungsdefinition für dieses Argument übergeben, öffnet ADO mithilfe der angegebenen Parameter eine neue Verbindung. Die [ActiveConnection](activeconnection-property-ado-md.md) -Eigenschaft entspricht das *ActiveConnection* -Argument.

## <a name="remarks"></a>Hinweise

Die **Open** -Methode erzeugt einen Fehler, wenn einer der Parameter ausgelassen wird und vor dem Öffnen des **Cellset** -Objekts der entsprechende Eigenschaftswert nicht festgelegt wurde.
