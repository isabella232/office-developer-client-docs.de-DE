---
title: CancelRecordChange-Makroaktion
TOCTitle: CancelRecordChange macro action
ms:assetid: 73031240-1ff6-660b-b25f-11a880df6031
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195846(v=office.15)
ms:contentKeyID: 48545626
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: ebbde6cee79aa822d710089d06aff39767413ccc
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59606968"
---
# <a name="cancelrecordchange-macro-action"></a>CancelRecordChange-Makroaktion


**Gilt für**: Access 2013, Office 2013

Mit der **CancelRecordChange** -Aktion können Sie die Änderungen an einem Datensatz in einem **[DatensatzErstellen](createrecord-data-block.md)** - oder **[BearbeitenDatensatz](editrecord-data-block.md)** -Datenblock abbrechen, bevor für diese ein Commit erfolgt ist.


> [!NOTE]
> [!HINWEIS] Die **AbbrechenDatensatzänderung** -Aktion ist nur in Datenmakros verfügbar.



## <a name="remarks"></a>HinwBemerkungeneise

Wenn Sie die **AbbrechenDatensatzänderung** -Aktion aufrufen, wird der **DatensatzErstellen** - oder **DatensatzBearbeiten** -Datenblock sofort beendet.

