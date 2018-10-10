---
title: Field.VisibleValue Property (DAO)
TOCTitle: VisibleValue Property
ms:assetid: e40fcb43-9a1d-69e7-1544-8f15ef21daf4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835776(v=office.15)
ms:contentKeyID: 48548332
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 892c7b41a692f353ee7e5bdd2191f6e21b8b4cf2
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25473407"
---
# <a name="fieldvisiblevalue-property-dao"></a>Field.VisibleValue Property (DAO)


**Betrifft**: Access 2013 | Office 2013

## <a name="syntax"></a>Syntax

*Ausdruck* . VisibleValue

*Ausdruck* Eine Variable, die ein **Field** -Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft enthält den Wert des Felds, der sich aktuell in der Datenbank auf dem Server befindet. Bei einer optimistischen Batchaktualisierung kann ein Konflikt auftreten, wenn ein zweiter Client dasselbe Feld und denselben Datensatz in dem Zeitraum ändert, in dem der erste Client die Daten abruft und versucht, die Daten zu aktualisieren. Wenn dies geschieht, kann auf den Wert, den der zweite Client festgelegt hat, über diese Eigenschaft zugegriffen werden.

