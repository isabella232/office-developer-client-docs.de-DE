---
title: Handler-Eigenschaft (RDS)
TOCTitle: Handler property (RDS)
ms:assetid: aaf8c8c6-f95b-3cf3-b3f6-203f37464c87
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249792(v=office.15)
ms:contentKeyID: 48546962
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 1ea6d8a4ba0bb4a2b9a5a61e8241e853408b6263
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59594209"
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
|*String* |Ein **String -Wert,** der den Namen des Handlers und alle Parameter enthält, die alle durch Kommas getrennt sind (z. B. "handlerName,parm1,parm2,...,parm *N*" ).|

## <a name="remarks"></a>HinwBemerkungeneise

Diese Eigenschaft unterstützt die Anpassung. Bei dieser Funktionalität muss die [CursorLocation](cursorlocation-property-ado.md)-Eigenschaft auf **adUseClient** festgelegt werden.

Der Name des Handlers und ggf. seiner Parameter werden durch Kommas (",") voneinander getrennt. Ein Semikolon an einer beliebigen Stelle in *String* führt zu unvorhersehbarem Verhalten. Sie können einen eigenen Handler schreiben, er muss jedoch die **IDataFactoryHandler**-Schnittstelle unterstützten.

Der Name des Standardhandlers lautet **MSDFMAP.Handler**, und sein Standardparameter ist eine Anpassungsdatei mit dem Namen **MSDFMAP.INI**. Rufen Sie mit dieser Eigenschaft alternative Anpassungsdateien auf, die vom Serveradministrator erstellt wurden.

Statt die **Handler**-Eigenschaft festzulegen, können Sie einen Handler und Parameter in der [ConnectionString](connectionstring-property-ado.md)-Eigenschaft angeben. Beispiel: "**Handler=**_handlerName,parm1,parm2,...;_".

