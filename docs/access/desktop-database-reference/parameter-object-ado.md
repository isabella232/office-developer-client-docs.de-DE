---
title: Parameter-Objekt (ADO)
TOCTitle: Parameter object (ADO)
ms:assetid: 7577598e-3d0c-30c6-5f24-1cfe98791798
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249481(v=office.15)
ms:contentKeyID: 48545676
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2000585a890256da878483b5538990c1898fc84a
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25927815"
---
# <a name="parameter-object-ado"></a>Parameter-Objekt (ADO)


**Betrifft**: Access 2013, Office 2013

Stellt einen Parameter oder ein Argument dar, der bzw. das einem [Command](command-object-ado.md)-Objekt zugeordnet ist, das auf einer parametrisierten Abfrage oder einer gespeicherten Prozedur basiert.

## <a name="remarks"></a>Hinweise

Zahlreiche Anbieter unterstützen parametrisierte Befehle. Dies sind Befehle, in denen die gewünschte Aktion einmal definiert wird, aber Variablen (oder Parameter) verwendet werden, um Details des Befehls zu ändern. Eine SQL SELECT-Anweisung kann z. B. einen Parameter verwenden, um die Übereinstimmungskriterien einer WHERE-Klausel zu definieren, und eine andere, um den Spaltennamen für eine SORT BY-Klausel festzulegen.

**Parameter** -Objekte stellen Parameter, die parametrisierten Abfragen zugeordnet sind, oder die Ein-/Ausgabeargumente und die Rückgabewerte von gespeicherten Prozeduren dar. Abhängig von der Funktionalität des Anbieters sind verschiedene Aufzählungen, Methoden oder Eigenschaften eines **Parameter** -Objekts möglicherweise nicht verfügbar.

Die Auflistungen, Methoden und Eigenschaften eines **Parameter** -Objekts ermöglichen Folgendes:

  - Festlegen oder Zurückgeben des Namens eines Parameters mit der [Name](name-property-ado.md)-Eigenschaft.

  - Festlegen oder Zurückgeben eines Parameterwerts mit der [Value](value-property-ado.md)-Eigenschaft. **Value** ist die Standardeigenschaft des **Parameter** -Objekts.

  - Festlegen oder Zurückgeben von Parametermerkmalen mit den Eigenschaften [Attributes](attributes-property-ado.md), [Direction](direction-property-ado.md), [Precision](precision-property-ado.md), [NumericScale](numericscale-property-ado.md), [Size](size-property-ado.md) und [Type](type-property-ado.md).

  - Übergeben von langen Binär- oder Zeichendaten an einen Parameter mit der [AppendChunk](appendchunk-method-ado.md)-Methode.

  - Zugreifen auf anbieterspezifische Attribute für die [Properties](properties-collection-ado.md)-Auflistung.

Wenn Sie die Namen und Eigenschaften der Parameter kennen, die der aufzurufenden gespeicherten Prozedur oder parametrisierten Abfrage zugeordnet sind, können Sie die [CreateParameter](createparameter-method-ado.md)-Methode verwenden, um **Parameter** -Objekte mit den betreffenden Eigenschaftswerten zu erstellen und sie mit der [Append](append-method-ado.md)-Methode der [Parameters](parameters-collection-ado.md)-Auflistung hinzufügen. Auf diese Weise können Sie Parameterwerte festlegen und zurückgeben, ohne die [Refresh](refresh-method-ado.md)-Methode für die **Parameters** -Auflistung aufzurufen, um die Parameterinformationen des Anbieters abzufragen, einem potenziell ressourcenintensiven Vorgang.

