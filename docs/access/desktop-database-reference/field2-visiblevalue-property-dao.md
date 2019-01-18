---
title: Field2.VisibleValue-Eigenschaft (DAO)
TOCTitle: VisibleValue Property
ms:assetid: 1e023a1a-fd49-7570-42bd-2f4c06ac5e5e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845809(v=office.15)
ms:contentKeyID: 48543611
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1101184
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 0161ea66068457b53a9667a6739c3a3a0458c8c5
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28721031"
---
# <a name="field2visiblevalue-property-dao"></a>Field2.VisibleValue-Eigenschaft (DAO)


**Betrifft**: Access 2013, Office 2013

## <a name="syntax"></a>Syntax

*Ausdruck* . VisibleValue

*Ausdruck* Eine Variable, die ein **Field2** -Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft enthält den Wert des Felds, der sich aktuell in der Datenbank auf dem Server befindet. Bei einer optimistischen Batchaktualisierung kann ein Konflikt auftreten, wenn ein zweiter Client dasselbe Feld und denselben Datensatz in dem Zeitraum ändert, in dem der erste Client die Daten abruft und versucht, die Daten zu aktualisieren. Wenn dies geschieht, kann auf den Wert, den der zweite Client festgelegt hat, über diese Eigenschaft zugegriffen werden.

