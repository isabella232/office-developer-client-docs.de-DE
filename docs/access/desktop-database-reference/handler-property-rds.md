---
title: Handler-Eigenschaft (RDS)
TOCTitle: Handler Property (RDS)
ms:assetid: aaf8c8c6-f95b-3cf3-b3f6-203f37464c87
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249792(v=office.15)
ms:contentKeyID: 48546962
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2a020dfa5935cfe6a0b942c5234eda2a91c40d51
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25474266"
---
# <a name="handler-property-rds"></a>Handler-Eigenschaft (RDS)


**Betrifft**: Access 2013 | Office 2013


Gibt den Name eines serverbasierten Anpassungsprogramms (Handlers) an, das die Funktionalität des [RDSServer.DataFactory](datafactory-object-rdsserver.md)-Objekts erweitert, sowie alle vom *Handler* verwendeten Parameter.

## <a name="syntax"></a>Syntax

*DataControl*. Handler = *Zeichenfolge*

## <a name="parameters"></a>Parameter

  - *DataControl*

  - Eine Objektvariable, die ein [RDS.DataControl](datacontrol-object-rds.md)-Objekt darstellt.

  - *String*

  - Ein **String** -Wert, der den Namen der Handler und Parameter, alle durch Kommas getrennt (beispielsweise "HandlerName, param1, param2,..., *N*Parameter") enthält.

## <a name="remarks"></a>Hinweise

Diese Eigenschaft unterstützt die Anpassung. Bei dieser Funktionalität muss die [CursorLocation](cursorlocation-property-ado.md)-Eigenschaft auf **adUseClient** festgelegt werden.

Der Name des Handlers und ggf. seiner Parameter werden durch Kommas (",") voneinander getrennt. Ein Semikolon an einer beliebigen Stelle in *String* führt zu unvorhersehbarem Verhalten. Sie können einen eigenen Handler schreiben, er muss jedoch die **IDataFactoryHandler**-Schnittstelle unterstützten.

Der Name des Standardhandlers lautet **MSDFMAP.Handler**, und sein Standardparameter ist eine Anpassungsdatei mit dem Namen **MSDFMAP.INI**. Rufen Sie mit dieser Eigenschaft alternative Anpassungsdateien auf, die vom Serveradministrator erstellt wurden.

Alternativ zum Festlegen der **Handler** -Eigenschaft ist ein Handler und-Parameter in der [ConnectionString](connectionstring-property-ado.md) -Eigenschaft angegeben. d. h., "**Handler = *** HandlerName, param1, param2,...;*".
