---
title: FixMAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 32676003-ba32-886f-1185-4760cb0e30e3
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 2aeca1a65a859ac9502995a463bc4869609bcd15
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334961"
---
# <a name="fixmapi"></a>FixMAPI

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Erstellt eine Sicherungskopie der aktuellen Kopie von MAPI32. dll auf dem Clientcomputer und stellt Mapi32. dll mit der MAPI-Stub-Bibliothek mapistub. dll wieder her.
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Exportiert von:  <br/> |mapistub. dll  <br/> |
|Aufgerufen von:  <br/> |Client  <br/> |
|Implementiert von:  <br/> |Windows  <br/> |
   
```cpp
DWORD STDAPICALLTYPE FixMAPI(void); 
```

## <a name="return-values"></a>Rückgabewerte

Wenn die Funktion erfolgreich ist, ist der Rückgabewert ein Wert ungleich NULL.
  
Wenn die Funktion fehlschlägt, ist der Rückgabewert NULL. Um erweiterte Fehlerinformationen abzurufen, rufen Sie die Microsoft Windows Software Development Kit (SDK)-Funktion, **[getlasterroraufzurufen](https://msdn.microsoft.com/library/ms679360.aspx)**. 
  
## <a name="remarks"></a>Bemerkungen

 **Fixmapi** ersetzt die aktuelle Mapi32. dll-Datei nicht, wenn die Datei schreibgeschützt ist. 
  
 **Fixmapi** ersetzt nicht die aktuelle Mapi32. dll, wenn Microsoft Exchange Server auf dem Computer installiert ist. 
  
Wenn **Fixmapi** eine Sicherungskopie der aktuellen Kopie von MAPI32. dll auf dem Computer erstellt, weist es der Sicherungskopie einen anderen Namen als "Mapi32. dll" zu. Anschließend werden nachfolgende Aufrufe für diese Assembly an die Sicherungskopie weitergeleitet. 
  
## <a name="see-also"></a>Siehe auch



[KB 256946: Sie erhalten eine Programmkonflikt-Fehlermeldung beim Starten von Outlook 2000](https://support.microsoft.com/kb/256946)
  
[KB 228457: Beschreibung des in Internet Explorer 5 enthaltenen Fixmapi. exe-Tools](https://support.microsoft.com/kb/228457)

