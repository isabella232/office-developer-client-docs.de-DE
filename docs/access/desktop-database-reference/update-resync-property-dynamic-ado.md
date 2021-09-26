---
title: Aktualisieren der dynamischen Resync-Eigenschaft (ADO)
TOCTitle: Update Resync dynamic property (ADO)
ms:assetid: 0af9cfd2-8042-65c9-cec6-77d2e7a88ad9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248842(v=office.15)
ms:contentKeyID: 48543166
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 5eed22559b0645cdae4498438fd6926136fb3303
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59631650"
---
# <a name="update-resync-dynamic-property-ado"></a>Aktualisieren der dynamischen Resync-Eigenschaft (ADO)


**Gilt für**: Access 2013, Office 2013

Es wird angegeben, ob auf die [UpdateBatch](updatebatch-method-ado.md)-Methode eine implizite [Resync](resync-method-ado.md)-Methodenoperation folgt, und es wird gegebenenfalls der Umfang der Operation angegeben.

## <a name="settings-and-return-values"></a>Einstellungen- und Rückgabewerte

Legt einen oder mehrere der [ADCPROP \_ UPDATERESYNC-ENUM-Werte \_ ](adcprop-updateresync-enum.md) fest oder gibt sie zurück.

## <a name="remarks"></a>Bemerkungen

Die Werte von ADCPROP \_ UPDATERESYNC \_ ENUM können kombiniert werden, mit Ausnahme von adResyncAll, das bereits die Kombination der restlichen Werte darstellt.

Mit der **adResyncConflicts** -Konstante werden die Neusynchronisierungswerte als zugrunde liegende Werte gespeichert, aber ausstehende Änderungen werden nicht außer Kraft gesetzt.

**Update Resync** ist eine dynamische Eigenschaft, die an die [Properties](recordset-object-ado.md)-Auflistung des [Recordset](properties-collection-ado.md)-Objekts angefügt wird, wenn die [CursorLocation](cursorlocation-property-ado.md)-Eigenschaft auf **adUseClient** festgelegt ist.

