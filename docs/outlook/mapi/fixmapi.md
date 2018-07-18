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
ms.openlocfilehash: 3c064301a18a8adbfb6109170ed16cb6981d96c2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791681"
---
# <a name="fixmapi"></a>FixMAPI

  
  
**Betrifft**: Outlook 
  
Erstellt eine Sicherungskopie der aktuellen Kopie von mapi32.dll auf dem Client, Computer und Wiederherstellung mapi32.dll mit der MAPI-Bibliothek Stub mapistub.dll.
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Vom exportiert werden:  <br/> |MAPISTUB.dll  <br/> |
|Aufgerufen von:  <br/> |Client  <br/> |
|Implementiert von:  <br/> |Windows  <br/> |
   
```cpp
DWORD STDAPICALLTYPE FixMAPI(void); 
```

## <a name="return-values"></a>Rückgabewerte

Wenn die Funktion erfolgreich ist, ist der Rückgabewert ein Wert ungleich NULL.
  
Wenn die Funktion fehlschlägt, ist der Rückgabewert 0 (null). Wenn Sie erweiterte Fehlerinformationen erhalten möchten, rufen Sie die Microsoft Windows Software Development Kit (SDK)-Funktion, **[GetLastError](http://msdn.microsoft.com/en-us/library/ms679360.aspx)**. 
  
## <a name="remarks"></a>Bemerkungen

 **Fixmapi.exe** ersetzt nicht die aktuelle Datei mapi32.dll, wenn die Datei als schreibgeschützt gekennzeichnet ist. 
  
 **Fixmapi.exe** ersetzt die aktuellen mapi32.dll nicht, wenn Microsoft Exchange Server auf dem Computer installiert ist. 
  
Wenn auf dem Computer eine Sicherungskopie der aktuellen Kopie von mapi32.dll für **Fixmapi.exe** ernannt werden, weist der Sicherungskopie einen Namen "mapi32.dll" unterscheidet. Klicken Sie dann weist es nachfolgende Aufrufe für diese Assembly in die Sicherungskopie vorgesehen ist. 
  
## <a name="see-also"></a>Siehe auch



[KB 256946: Sie erhalten eine Fehlermeldung zu eine Konflikt angezeigt, beim start von Outlook 2000](http://support.microsoft.com/kb/256946)
  
[KB 228457: Beschreibung des Fixmapi.exe Tools enthalten, mit InternetExplorer 5](http://support.microsoft.com/kb/228457)

