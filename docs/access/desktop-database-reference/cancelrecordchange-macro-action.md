---
title: AbbrechenDatensatzänderung-Makroaktion
TOCTitle: CancelRecordChange Macro Action
ms:assetid: 73031240-1ff6-660b-b25f-11a880df6031
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195846(v=office.15)
ms:contentKeyID: 48545626
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8fe474f9ba7250e3225bc73460c6d192800c861b
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25474174"
---
# <a name="cancelrecordchange-macro-action"></a>AbbrechenDatensatzänderung-Makroaktion


**Betrifft**: Access 2013 | Office 2013

Mit der **CancelRecordChange** -Aktion können Sie die Änderungen an einem Datensatz in einem **[DatensatzErstellen](createrecord-data-block.md)** - oder **[BearbeitenDatensatz](editrecord-data-block.md)** -Datenblock abbrechen, bevor für diese ein Commit erfolgt ist.


> [!NOTE]
> <P>[!HINWEIS] Die <STRONG>AbbrechenDatensatzänderung</STRONG> -Aktion ist nur in Datenmakros verfügbar.</P>



## <a name="remarks"></a>Hinweise

Wenn Sie die **AbbrechenDatensatzänderung** -Aktion aufrufen, wird der **DatensatzErstellen** - oder **DatensatzBearbeiten** -Datenblock sofort beendet.

