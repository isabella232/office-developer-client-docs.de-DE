---
title: IABContainerCopyEntries
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABContainer.CopyEntries
api_type:
- COM
ms.assetid: 4e775228-5ceb-4002-9b68-999fb5889b86
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: ddb730ed92db4c8d281e7c8d5d9b18bc44505598
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346396"
---
# <a name="iabcontainercopyentries"></a>IABContainer::CopyEntries

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Kopiert einen oder mehrere Einträge, in der Regel Messagingbenutzer oder Verteilerlisten.
  
```cpp
HRESULT CopyEntries(
  LPENTRYLIST lpEntries,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameter

 _lpEntries_
  
> in Ein Zeiger auf ein Array von [entrylist](entrylist.md) -Strukturen, das die Eintragsbezeichner der zu kopierende Einträge enthält. 
    
 _ulUIParam_
  
> in Das Handle für das übergeordnete Fenster aller von dieser Methode angezeigten Dialogfelder oder Fenster. Der _ulUIParam_ -Parameter muss NULL sein, wenn das AB_NO_DIALOG-Flag im _ulFlags_ -Parameter festgelegt ist. 
    
 _lpProgress_
  
> in Ein Zeiger auf ein Progress-Objekt, das eine Statusanzeige oder NULL anzeigt. Wenn _lpProgress_ ist, sollte eine Statusanzeige mithilfe des von MAPI über die [IMAPISupport::D oprogressdialog](imapisupport-doprogressdialog.md) -Methode bereitgestellten Progress-Objekts angezeigt werden. Der _lpProgress_ -Parameter wird ignoriert, wenn das AB_NO_DIALOG-Flag in _ulFlags_festgelegt ist.
    
 _ulFlags_
  
> in Eine Bitmaske von Flags, die die Ausführung des Kopiervorgangs steuert. Die folgenden Flags können festgelegt werden:
    
AB_NO_DIALOG 
  
> UnterDrückt die Anzeige einer Statusanzeige. Wenn dieses Flag nicht festgelegt ist, wird eine Statusanzeige angezeigt.
    
CREATE_CHECK_DUP_LOOSE 
  
> Gibt an, dass eine Überprüfung der doppelten Eingabe durchgeführt werden soll. Die Implementierung von Loose Duplicate entry checking ist Anbieter spezifisch. Ein Anbieter kann beispielsweise eine lockere Übereinstimmung als zwei Einträge definieren, die den gleichen Anzeigenamen aufweisen.
    
CREATE_CHECK_DUP_STRICT 
  
> Gibt an, dass eine strikte doppelte Eingabeüberprüfung durchgeführt werden soll. Die Implementierung einer strengen doppelten Eintrags Überprüfung ist Anbieter spezifisch. Ein Anbieter kann beispielsweise eine strikte Übereinstimmung als zwei Einträge definieren, die den gleichen Anzeigenamen und die gleiche Messaging Adresse aufweisen.
    
CREATE_REPLACE 
  
> Gibt an, dass ein neuer Eintrag eine vorhandene ersetzen soll, wenn festgestellt wird, dass die beiden Duplikate sind.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Kopiervorgang war erfolgreich.
    
MAPI_W_PARTIAL_COMPLETION 
  
> Der Kopiervorgang war insgesamt erfolgreich, aber mindestens einer der Einträge konnte nicht kopiert werden. Wenn dieser Wert zurückgegeben wird, sollte der Aufruf als erfolgreich behandelt werden. Verwenden Sie das **HR_FAILED** -Makro, um diesen Wert zu testen. Weitere Informationen finden Sie unter [Verwenden von Makros zur Fehlerbehandlung](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Bemerkungen

Die **IABContainer:: CopyEntries** -Methode kopiert Einträge aus demselben Container oder aus einem anderen Container. Ein Aufruf von **CopyEntries** ist funktionell gleichbedeutend mit der folgenden Aufrufe für jeden Eintrag kopiert werden: 
  
1. Die [IABContainer:: CreateEntry](iabcontainer-createentry.md) -Methode zum Erstellen des neuen Eintrags. 
    
2. Die [IMAPIProp::](imapiprop-getprops.md) GetProps-Methode zum Lesen von Eigenschaften aus dem zu kopierenden Eintrag. 
    
3. Die [IMAPIProp::](imapiprop-setprops.md) SetProps-Methode zum Schreiben von Eigenschaften in den neuen Eintrag. 
    
4. Die [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) -Methode des neuen Eintrags zum Durchführen eines Speichers. 
    
5. Die [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28VS.85%29.aspx) -Methode des neuen Eintrags zum Freigeben des Container-Verweises. 
    
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Alle Container, die die **IABContainer:: CopyEntries** -Methode unterstützen, müssen geändert werden können. Legen Sie das AB_MODIFIABLE-Flag ihres Containers in seiner **PR_CONTAINER_FLAGS** ([pidtagcontainerflags (](pidtagcontainerflags-canonical-property.md))-Eigenschaft fest, um anzugeben, dass es veränderbar ist. 
  
Sie müssen alle Flags unterstützen. die Interpretation und Verwendung dieser Flags ist jedoch implementierungsspezifisch, d. h., Sie können bestimmen, welche Semantik die Flags CREATE_CHECK_DUP_LOOSE und CREATE_CHECK_DUP_STRICT im Kontext ihrer Implementierung bedeuten. Wenn Sie nicht feststellen können, ob ein Eintrag ein Duplikat ist, können Sie immer zulassen, dass der Eintrag kopiert wird. 
  
Wenn das CREATE_REPLACE-Flag festgelegt ist, kopieren Sie den Eintrag immer unabhängig davon, ob CREATE_CHECK_DUP_LOOSE oder CREATE_CHECK_DUP_STRICT festgelegt ist und ob der Eintrag ein Duplikat ist. 
  
Wenn CREATE_REPLACE nicht festgelegt ist und CREATE_CHECK_DUP_STRICT festgelegt ist, überprüfen Sie, ob Duplikate vorhanden sind. Wenn ein Eintrag als Duplikat festgelegt wurde, kopieren Sie den Eintrag nicht. 
  
Sie müssen CREATE_REPLACE nicht unterstützen; nicht die Unterstützung von CREATE_REPLACE, dass Sie Sie bedenkenlos ignorieren und immer eine Kopie ausführen können. 
  
Geben Sie die Warnung MAPI_W_PARTIAL_COMPLETION nur dann zurück, wenn ein nicht doppelter Eintrag nicht kopiert werden kann. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Verwenden Sie die CREATE_CHECK_DUP_LOOSE-und CREATE_CHECK_DUP_STRICT-Flags, um dem Anbieter anzuzeigen, wie der Container die Überprüfung durch doppelte Eingabe ausführen soll. Wenn ein Eintrag hinzugefügt werden muss, unabhängig davon, ob es sich um ein Duplikat handelt, legen Sie entweder keine dieser Flags fest oder legen Sie das CREATE_REPLACE-Flag fest. CREATE_REPLACE gibt an, dass es Ihnen egal ist, ob ein Eintrag ein Duplikat ist; Sie möchten immer, dass der ursprüngliche Eintrag ersetzt wird. 
  
## <a name="see-also"></a>Siehe auch



[ENTRYLIST](entrylist.md)
  
[IABContainer::CreateEntry](iabcontainer-createentry.md)
  
[IMAPIProgress : IUnknown](imapiprogressiunknown.md)
  
[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IABContainer : IMAPIContainer](iabcontainerimapicontainer.md)

