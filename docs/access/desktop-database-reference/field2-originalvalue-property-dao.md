---
title: Field2.OriginalValue-Eigenschaft (DAO)
TOCTitle: OriginalValue Property
ms:assetid: 10fed55e-c938-2ae6-8fd2-996745a63da3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845353(v=office.15)
ms:contentKeyID: 48543306
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1101183
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: f385f2f16a9cd28f22891fc753b1a537fda1f346
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59565373"
---
# <a name="field2originalvalue-property-dao"></a>Field2.OriginalValue-Eigenschaft (DAO)


**Gilt für**: Access 2013, Office 2013

## <a name="syntax"></a>Syntax

*Ausdruck* . OriginalValue

*Ausdruck* Eine Variable, die ein **Field2**-Objekt darstellt.

## <a name="remarks"></a>HinwBemerkungeneise

Bei einer optimistischen Batchaktualisierung können Konflikte auftreten, wenn in der Zeitspanne, in der ein erster Client Daten abruft und eine Aktualisierung versucht, ein zweiter Client dasselbe Feld und den Datensatz ändert. Die **OriginalValue**-Eigenschaft enthält den Wert des Felds zu dem Zeitpunkt, zu dem der **Update**-Batchvorgang begann. Falls dieser Wert nicht mit dem tatsächlich in der Datenbank vorhandenen Wert übereinstimmt, während der **Update**-Batchvorgang versucht, Daten in die Datenbank zu schreiben, tritt ein Konflikt auf. In diesem Fall kann mithilfe der **VisibleValue**-Eigenschaft auf den neuen Wert in der Datenbank zugegriffen werden.

