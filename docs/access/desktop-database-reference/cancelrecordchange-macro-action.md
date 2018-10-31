---
title: AbbrechenDatensatzänderung-Makroaktion
TOCTitle: CancelRecordChange Macro Action
ms:assetid: 73031240-1ff6-660b-b25f-11a880df6031
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195846(v=office.15)
ms:contentKeyID: 48545626
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ddf6a6eb71d60fb98d92a9ce18bfd871f298f702
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25864207"
---
# <a name="cancelrecordchange-macro-action"></a>AbbrechenDatensatzänderung-Makroaktion


**Betrifft**: Access 2013 | Office 2013

Mit der **CancelRecordChange** -Aktion können Sie die Änderungen an einem Datensatz in einem **[DatensatzErstellen](createrecord-data-block.md)** - oder **[BearbeitenDatensatz](editrecord-data-block.md)** -Datenblock abbrechen, bevor für diese ein Commit erfolgt ist.


> [!NOTE]
> [!HINWEIS] Die **AbbrechenDatensatzänderung** -Aktion ist nur in Datenmakros verfügbar.



## <a name="remarks"></a>Hinweise

Wenn Sie die **AbbrechenDatensatzänderung** -Aktion aufrufen, wird der **DatensatzErstellen** - oder **DatensatzBearbeiten** -Datenblock sofort beendet.

