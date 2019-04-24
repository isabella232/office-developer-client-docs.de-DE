---
title: QueryDef. Schließ-Methode (DAO)
TOCTitle: Close Method
ms:assetid: b2b63462-453d-9e2b-0bb3-69a4a7a6ecef
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822031(v=office.15)
ms:contentKeyID: 48547179
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052976
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 4d50fa52ff4f5d669b062a052bf3e59a28a9e732
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303304"
---
# <a name="querydefclose-method-dao"></a>QueryDef. Schließ-Methode (DAO)


**Gilt für**: Access 2013, Office 2013

Schließt ein geöffnetes **QueryDef**-Objekt.

## <a name="syntax"></a>Syntax

*Ausdruck* . Schließen

*Ausdruck* Eine Variable, die ein **QueryDef** -Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

Ist das **QueryDef**-Objekt beim Verwenden von **Close** bereits geschlossen, tritt ein Laufzeitfehler auf.

Eine Alternative zur **Schließ** -Methode besteht darin, den Wert einer Objektvariable auf **Nothing** festzulegen (Set dbsTemp = Nothing).

