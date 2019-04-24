---
title: Handler-Eigenschaft (RDS)
TOCTitle: Handler property (RDS)
ms:assetid: aaf8c8c6-f95b-3cf3-b3f6-203f37464c87
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249792(v=office.15)
ms:contentKeyID: 48546962
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c3ad91f0a288b9908a5af5f92d7bfca3b23cdfe9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292069"
---
# <a name="handler-property-rds"></a>Handler-Eigenschaft (RDS)

**Gilt für**: Access 2013, Office 2013

Gibt den Name eines serverbasierten Anpassungsprogramms (Handlers) an, das die Funktionalität des [RDSServer.DataFactory](datafactory-object-rdsserver.md)-Objekts erweitert, sowie alle vom *Handler* verwendeten Parameter.

## <a name="syntax"></a>Syntax

*DataControl*. Handler = *Zeichenfolge*

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*DataControl* |Eine Objektvariable, die ein [RDS.DataControl](datacontrol-object-rds.md)-Objekt darstellt.|
|*String* |Ein **String** -Wert, der den Namen des Handlers und alle Parameter enthält, die alle durch Kommata getrennt sind (beispielsweise "Handlername, Parm1, Parameter2,..., parm *N*").|

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft unterstützt die Anpassung. Bei dieser Funktionalität muss die [CursorLocation](cursorlocation-property-ado.md)-Eigenschaft auf **adUseClient** festgelegt werden.

Der Name des Handlers und ggf. seiner Parameter werden durch Kommas (",") voneinander getrennt. Ein Semikolon an einer beliebigen Stelle in *String* führt zu unvorhersehbarem Verhalten. Sie können einen eigenen Handler schreiben, er muss jedoch die **IDataFactoryHandler**-Schnittstelle unterstützten.

Der Name des Standardhandlers lautet **MSDFMAP.Handler**, und sein Standardparameter ist eine Anpassungsdatei mit dem Namen **MSDFMAP.INI**. Rufen Sie mit dieser Eigenschaft alternative Anpassungsdateien auf, die vom Serveradministrator erstellt wurden.

Die Alternative zum Festlegen der **Handler** -Eigenschaft besteht darin, einen Handler und Parameter in der [ConnectionString](connectionstring-property-ado.md) -Eigenschaft anzugeben. Das heißt, "**Handler = * * * Handlername, Parm1, parameter2,...;*".

