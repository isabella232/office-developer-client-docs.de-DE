---
title: FixMAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 32676003-ba32-886f-1185-4760cb0e30e3
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: d40c06b5bd7e2d2523fb81b702c513c6521518e4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59621094"
---
# <a name="fixmapi"></a>FixMAPI

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Erstellt eine Sicherungskopie der aktuellen Kopie von mapi32.dll auf dem Clientcomputer und stellt mapi32.dll mit der MAPI-Stubbibliothek mapistub.dll wieder her.
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Exportiert von:  <br/> |mapistub.dll  <br/> |
|Aufgerufen von:  <br/> |Client  <br/> |
|Implementiert von:  <br/> |Windows  <br/> |
   
```cpp
DWORD STDAPICALLTYPE FixMAPI(void); 
```

## <a name="return-values"></a>Rückgabewerte

Wenn die Funktion erfolgreich ist, ist der Rückgabewert ein Wert ungleich Null.
  
Wenn die Funktion fehlschlägt, ist der Rückgabewert Null. Rufen Sie zum Abrufen erweiterter Fehlerinformationen die Microsoft Windows Software Development Kit (SDK)-Funktion **[GetLastError](https://msdn.microsoft.com/library/ms679360.aspx)** auf. 
  
## <a name="remarks"></a>Bemerkungen

 **FixMAPI** ersetzt nicht die aktuelle mapi32.dll Datei, wenn die Datei als schreibgeschützt markiert ist. 
  
 **FixMAPI** ersetzt nicht die aktuelle mapi32.dll, wenn Microsoft Exchange Server auf dem Computer installiert ist. 
  
Wenn **FixMAPI** eine Sicherungskopie der aktuellen Kopie von mapi32.dll auf dem Computer erstellt, wird der Sicherungskopie ein anderer Name als "mapi32.dll" zugewiesen. Anschließend werden nachfolgende Aufrufe, die für diese Assembly vorgesehen sind, an die Sicherungskopie gesendet. 
  
## <a name="see-also"></a>Siehe auch



[KB 256946: Beim Starten von Outlook 2000 wird eine Programmkonflikt-Fehlermeldung angezeigt.](https://support.microsoft.com/kb/256946)
  
[KB 228457: Beschreibung des in Internet Explorer 5 enthaltenen Fixmapi.exe-Tools](https://support.microsoft.com/kb/228457)

