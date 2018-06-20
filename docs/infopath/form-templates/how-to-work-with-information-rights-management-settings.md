---
title: Arbeiten Sie mit IRM-Einstellungen für die Verwaltung
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- Verwaltung von Informationsrechten [Infopath 2007] InfoPath 2007, Information Rights Management, IRM [InfoPath 2007]
localization_priority: Normal
ms.assetid: 4ad91898-b23e-4410-8839-a65259e53d37
description: 'Es stehen zwei Arten von Einstellungen (Information Rights Management, IRM) in Microsoft InfoPath: eines für den Schutz der Zugriff auf InfoPath-Formularvorlagen und eines zum Steuern der Zugriff auf und Aktionen auf Formulardaten in ausgefüllten Formulare enthalten sind.'
ms.openlocfilehash: 4e6fdac6a0b2b5cd6a29de948cc9dbbd01a407d8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790775"
---
# <a name="work-with-information-rights-management-settings"></a>Arbeiten Sie mit IRM-Einstellungen für die Verwaltung

Es stehen zwei Arten von Einstellungen (Information Rights Management, IRM) in Microsoft InfoPath: eines für den Schutz der Zugriff auf InfoPath-Formularvorlagen und eines zum Steuern der Zugriff auf und Aktionen auf Formulardaten in ausgefüllten Formulare enthalten sind.
  
> [!NOTE]
> Das Einschränken der Berechtigung ist nur für Formularvorlagen verfügbar, die mit dem InfoPath-Editor kompatibel sind. Von browserkompatiblen Formularvorlagen wird IRM nicht unterstützt. 
  
## <a name="adding-the-manage-credentials-command-to-the-quick-access-toolbar"></a>Hinzufügen des Befehls "Anmeldeinformationen verwalten" zur Symbolleiste für den Schnellzugriff

Der **Anmeldeinformationen verwalten** -Befehl verwendet, um IRM-Einstellungen entwickelt, beim Entwerfen einer Formularvorlage ist nicht standardmäßig verfügbar. Gehen Sie folgendermaßen vor, um es der **Symbolleiste für den Schnellzugriff**hinzufügen.
  
### <a name="add-the-manage-credentials-command-to-the-quick-access-toolbar"></a>Hinzufügen des Befehls "Anmeldeinformationen verwalten" zur Symbolleiste für den Schnellzugriff

1.  Klicken Sie auf den Pfeil am rechten Ende der **Symbolleiste für den Schnellzugriff** , ziehen Sie nach unten im Menü **Symbolleiste für den Schnellzugriff anpassen** , und klicken Sie dann auf **Weitere Befehle**.
    
2. In der Liste **Befehle auswählen** die Option **Alle Befehle**aus.
    
3. Führen Sie einen Bildlauf nach unten zu **Anmeldeinformationen verwalten**, und klicken Sie dann auf **Hinzufügen**.
    
4. Klicken Sie auf **OK**.
    
Weitere Informationen zur Verwendung von Befehls **Anmeldeinformationen verwalten** und des Dialogfelds **Berechtigung** in InfoPath im Feld, finden Sie im Thema "Erstellen eines Formulars mit eingeschränkter Berechtigung" in InfoPath. 
  
## <a name="the-irm-object-model"></a>Das IRM-Objektmodell

Verwenden Sie [Permission](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.aspx) -Klasse, um die [UserPermissionCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermissionCollection.aspx) und IRM-berechtigungseinstellungen zugreifen, die auf ein Formular angewendet werden kann. Um eine Formularvorlage zugeordneten **Permission** -Objekt zuzugreifen, verwenden Sie die [Permission](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Permission.aspx) -Eigenschaft der [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) -Klasse. Das zurückgegebene **Permission** -Objekt bietet Zugriff auf die Auflistung von [UserPermission](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermission.aspx) -Objekte, die der Formularvorlage zugeordneten und jede mit dieser Vorlage erstellte Formularinstanz. 
  
Die **Permission** -Objekt und seine Eigenschaften und Methoden stehen zur Verfügung, ob Berechtigungen auf der aktiven Formularvorlage eingeschränkt werden. Verwenden Sie die [Enabled](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.Enabled.aspx) -Eigenschaft, um zu bestimmen, ob ein Formular über eingeschränkte Berechtigungen verfügt. 
  
Berechtigungen für ein Formular werden auf eine der folgenden Arten mithilfe von Eigenschaften und Methoden der Permission-Klasse aktiviert:
  
Die **Enabled** -Eigenschaft ist auf **true**festgelegt.
  
[DocumentAuthor](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.DocumentAuthor.aspx) -Eigenschaft ist festgelegt. 
  
Die [RequestPermissionUrl](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.RequestPermissionUrl.aspx) -Eigenschaft ist festgelegt. 
  
Die [StoreLicenses](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.StoreLicenses.aspx) -Eigenschaft wird auf **true** oder **false**festgelegt.
  
Die [ApplyPolicy](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.ApplyPolicy.aspx) -Methode aufgerufen wird. 
  
> [!NOTE]
> Wenn der Windows-Rechteverwaltungsclient nicht auf dem Computer des Benutzers installiert ist, löst die Verwendung der **Permission** -Klasse eine Ausnahme. 
  
Verwenden Sie die Klassen **UserPermissionCollection** und **UserPermission** , um programmgesteuert mit IRM-Einstellungen einzelner Benutzer in Formularen zu arbeiten. 
  
Ein **UserPermission** -Objekt verbindet einen Satz von Berechtigungen für das aktuelle Formular mit einem einzelnen Benutzer und einem optionalen Ablaufdatum. Verwenden Sie die [Add](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermissionCollection.Add.aspx) -Methode der **UserPermissionCollection** -Klasse hinzugefügt und einem Benutzer einen Satz von Berechtigungen für das aktuelle Formular erteilt. Verwenden Sie die Methode [Entfernen](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermissionCollection.Remove.aspx) der **UserPermissionCollection** -Klasse, um einen Benutzer und Berechtigungen des Benutzers zu entfernen. Während einige Berechtigungen über die Benutzeroberfläche für alle Benutzer, wie etwa drucken und Ablauf Datum, gelten können die **UserPermission** und **UserPermissionCollection** -Klasse Sie jeden Benutzer einzeln mit pro Benutzer zuweisen Ablaufdatum. Das Objektmodell ermöglicht Entwicklern zum Aufzählen von berechtigungseinstellungen in einem Formular und Funktionalität bereitzustellen, mit der Benutzer des Formulars zum Hinzufügen von Berechtigungen auf das Formular, ohne den Aufgabenbereich **Formular Berechtigung** oder im Dialogfeld **Berechtigung** verwenden können. 
  
> [!NOTE]
> Berechtigungen können nicht angewendet werden, wenn ein Formular im Vorschaumodus befindet. Aus diesem Grund sind alle Eigenschaften der **Permission** -Klasse schreibgeschützt, wenn die Vorschau eines Formulars angezeigt. Im Vorschaumodus die **Enabled** -Eigenschaft gibt immer **false**zurück und Code versucht, diese Einstellung ändern, eine **System.Runtime.InteropServices.COMException** wird ausgelöst, und der Fehler "die Eigenschaftsmethode ist nicht verfügbar in der Vorschau Modus"zurückgegeben. In ähnlicher Weise werden die Methoden im Zusammenhang mit den Klassen **UserPermission** und **UserPermissionCollection** diese Fehlermeldung angezeigt, wenn im Vorschaumodus verwendet ebenfalls zurückgegeben. 
  
### <a name="overview-of-the-permission-class"></a>Übersicht über die "Permission"-Klasse

Die **UserPermissionCollection** -Klasse stellt die folgenden Eigenschaften und eine Methode bereit. 
  
|**Name**|**Beschreibung**|
|:-----|:-----|
|[ApplyPolicy (](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.ApplyPolicy.aspx) Methode)  <br/> |Wendet eine Richtlinie auf das Formular mithilfe einer Richtlinienvorlagendatei an.  <br/> |
|[DocumentAuthor](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.DocumentAuthor.aspx) -Eigenschaft  <br/> |Dient zum Abrufen oder festlegen den Autor des aktuellen Formulars als e-Mail-Adresse.  <br/> |
|[Enabled](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.Enabled.aspx) -Eigenschaft  <br/> |Ruft ab oder legt fest, ob die durch das **Permission** -Objekt dargestellten berechtigungseinstellungen für das aktuelle Formular aktiviert sind.  <br/> |
|[PermissionFromPolicy](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.PermissionFromPolicy.aspx) -Eigenschaft  <br/> |Ruft ab, ob eine Berechtigungsrichtlinie auf dem aktuellen Formular angewendet wurde, oder legt diese Einstellung fest.  <br/> |
|[PolicyDescription](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.PolicyDescription.aspx) -Eigenschaft  <br/> |Ruft eine Beschreibung der Richtlinie ab, die auf dem aktuellen Formular angewendet wurde.   <br/> |
|[PolicyName](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.PolicyName.aspx) -Eigenschaft  <br/> |Ruft den Namen der Richtlinie ab, die auf dem aktuellen Formular angewendet wurde.  <br/> |
|[RequestPermissionUrl](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.RequestPermissionUrl.aspx) -Eigenschaft  <br/> |Ruft ab oder legt fest, die Datei, URL oder e-Mail-Adresse für Benutzer wenden müssen, die zusätzliche Berechtigungen für das aktuelle Formular benötigen.  <br/> |
|[StoreLicenses](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.StoreLicenses.aspx) -Eigenschaft  <br/> |Ruft ab, ob die Benutzerlizenz zum Anzeigen des aktuellen Formulars zwischengespeichert werden soll, um die Offlineanzeige zuzulassen, wenn der Benutzer keine Verbindung zu einem Rechteverwaltungsserver herstellen kann, oder legt diese Einstellung fest.   <br/> |
|[UserPermissions](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.UserPermissions.aspx) -Eigenschaft  <br/> |Ruft ein **UserPermissionCollection** -Objekt für das aktuelle Formular ab.  <br/> |
   
### <a name="overview-of-the-userpermissioncollection-class"></a>Übersicht über die "UserPermissionCollection"-Klasse

Die **UserPermissionCollection** -Klasse bietet die folgenden Eigenschaften und Methoden. 
  
|**Name**|**Beschreibung**|
|:-----|:-----|
|[Add](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermissionCollection.Add.aspx) -Methode (+ 3 Überladungen)  <br/> |Fügt dem aktuellen Formular einen neuen Benutzer hinzu; optional können Berechtigungen und ein Ablaufdatum angegeben werden.  <br/> |
|[Remove](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermissionCollection.Remove.aspx)-Methode  <br/> |Entfernt das **UserPermission** -Objekt mit der angegebenen **Benutzer-ID** aus der Auflistung.  <br/> |
|[RemoveAll](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermissionCollection.RemoveAll.aspx) -Methode  <br/> |Entfernt alle **UserPermission** -Objekte aus der Auflistung.  <br/> |
|[Count](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermissionCollection.Count.aspx)-Eigenschaft  <br/> |Ruft die Anzahl der **UserPermission** -Objekte in der Auflistung ab.  <br/> |
|[Item](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermissionCollection.Item.aspx) -Eigenschaft (+ 1 Überladung)  <br/> |Ruft ein **UserPermission** -Objekt ab.  <br/> |
   
### <a name="overview-of-the-userpermission-class"></a>Übersicht über die "UserPermission"-Klasse

Die **UserPermission** -Klasse stellt die folgenden Eigenschaften und eine Methode bereit. 
  
|**Name**|**Beschreibung**|
|:-----|:-----|
|[Remove](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermission.Remove.aspx)-Methode  <br/> |Entfernt das aktuelle **UserPermission** -Objekt aus den Berechtigungen des Formulars.  <br/> |
|[ExpirationDate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermission.ExpirationDate.aspx) -Eigenschaft  <br/> |Ruft ab oder legt das optionale Ablaufdatum für die Berechtigungen auf dem aktuellen Formular für den Benutzer einer Instanz der **UserPermission** -Klasse zugeordnet.  <br/> |
|[Permission](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermission.Permission.aspx) -Eigenschaft  <br/> |Dient zum Abrufen oder Festlegen eines Werts, der Darstellung der Berechtigungen auf dem aktuellen Formular für den Benutzer einer Instanz der **UserPermission** -Klasse zugeordnet.  <br/> |
|[UserId](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermission.UserId.aspx) -Eigenschaft  <br/> |Ruft die e-Mail-Adresse des Benutzers, dessen Berechtigungen für das aktuelle Formular durch das angegebene **UserPermission** -Objekt bestimmt werden.  <br/> |
   
### <a name="the-permissiontype-enumeration"></a>Die "PermissionType"-Enumeration

Berechtigungen eines Benutzers festgelegt sind, oder Lesen [PermissionType](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.PermissionType.aspx) Enumeration-Werte verwenden. 
  
|**Name**|**Beschreibung**|
|:-----|:-----|
|**PermissionType.Change** <br/> |Ermöglicht Benutzern das anzeigen, bearbeiten, kopieren, und speichern, jedoch nicht Drucken eines Formulars. Entspricht der **Lesen**, kombiniert Berechtigungen **Bearbeiten**, **Speichern**und **extrahieren** .  <br/> |
|**PermissionType.Edit** <br/> |Ermöglicht dem Benutzer das Bearbeiten des Formulars.  <br/> |
|**PermissionType.Extract** <br/> |Ermöglicht einem Benutzer mit der Berechtigung **Lesen** Kopieren des Inhalts in der Form.  <br/> |
|**PermissionType.FullControl** <br/> |Ermöglicht dem Benutzer das Hinzufügen, Ändern oder Entfernen von Berechtigungen für andere Benutzer eines Formulars.  <br/> |
|**PermissionType.ObjectModel** <br/> |Ermöglicht einem Benutzer das Formulardokument programmgesteuert über das Objektmodell zugreifen. Benutzer ohne die Berechtigung **ObjectModel** können nicht das Objektmodell verwenden, um ihre eigenen Berechtigungen zu bestimmen.  <br/> |
|**PermissionType.Print** <br/> |Ermöglicht dem Benutzer das Drucken des Formulars.  <br/> |
|**PermissionType.Read** <br/> |Ermöglicht dem Benutzer das Lesen (Ansicht) das Formular. (Die Berechtigungen **Lesen** und **Anzeigen** sind gleichwertig.)  <br/> |
|**PermissionType.Save** <br/> |Ermöglicht dem Benutzer das Speichern des Formulars.  <br/> |
|**PermissionType.View** <br/> |Ermöglicht es dem Benutzer zur Ansicht (Lesen) das Formular. (Die Berechtigungen **Lesen** und **Anzeigen** sind gleichwertig.)  <br/> |
   
### <a name="example"></a>Beispiel

Im folgenden Beispiel durch Klicken auf die **Schaltfläche** -Steuerelement das **UserPermissionsCollection** für das aktuelle Formular abgerufen, fügt weist einem Benutzer das Change-Zugriffsebene und ein Ablaufdatum von zwei Tagen ab dem aktuellen Datum festgelegt. 
  
```cs
public void CTRL1_Clicked(object sender, ClickedEventArgs e)
{
   string strExpirationDate = DateTime.Today.AddDays(2).ToString();
   DateTime dtExpirationDate = DateTime.Parse(strExpirationDate);
   this.Permission.UserPermissions.Add("someone@example.com", 
      PermissionType.Change, dtExpirationDate);
}
```

```vb
Public Sub CTRL1_Clicked(ByVal sender As Object, _
   ByVal e As ClickedEventArgs)
   Dim strExpirationDate As String = _
      DateTime.Today.AddDays(2).ToString()
   dtExpirationDate As DateTime = DateTime.Parse(strExpirationDate)
   Me.Permission.UserPermissions.Add("someone@example.com", _
      PermissionType.Change, dtExpirationDate)
End Sub
```


