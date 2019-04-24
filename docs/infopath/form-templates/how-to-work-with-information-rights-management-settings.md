---
title: Arbeiten mit Einstellungen für die Verwaltung von Informationsrechten
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- Verwaltung von Informationsrechten [InfoPath 2007], InfoPath 2007, Verwaltung von Informationsrechten, IRM [InfoPath 2007]
localization_priority: Normal
ms.assetid: 4ad91898-b23e-4410-8839-a65259e53d37
description: 'In Microsoft InfoPath stehen zwei Arten von IRM-Einstellungen (Information Rights Management, Verwaltung von Informationsrechten) zur Verfügung: eine zum Schützen des Zugriffs auf InfoPath-Formularvorlagen und eine für die Steuerung des Zugriffs auf und der Aktionen auf Formulardaten, die in ausgefüllten Formularen enthalten sind.'
ms.openlocfilehash: 6f7317cfdc4e6bfc89482e813b1670c8b8861a6b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299790"
---
# <a name="work-with-information-rights-management-settings"></a>Arbeiten mit Einstellungen für die Verwaltung von Informationsrechten

In Microsoft InfoPath stehen zwei Arten von IRM-Einstellungen (Information Rights Management, Verwaltung von Informationsrechten) zur Verfügung: eine zum Schützen des Zugriffs auf InfoPath-Formularvorlagen und eine für die Steuerung des Zugriffs auf und der Aktionen auf Formulardaten, die in ausgefüllten Formularen enthalten sind.
  
> [!NOTE]
> Das Einschränken der Berechtigung ist nur für Formularvorlagen verfügbar, die mit dem InfoPath-Editor kompatibel sind. Von browserkompatiblen Formularvorlagen wird IRM nicht unterstützt. 
  
## <a name="adding-the-manage-credentials-command-to-the-quick-access-toolbar"></a>Hinzufügen des Befehls "Anmeldeinformationen verwalten" zur Symbolleiste für den Schnellzugriff

Der Befehl zum **Verwalten von Anmeldeinformationen** , der zum Arbeiten mit IRM-Einstellungen beim Entwerfen einer Formularvorlage verwendet wird, ist standardmäßig nicht verfügbar. Führen Sie die folgenden Schritte aus, um Sie der **Symbolleiste für den Schnellzugriff**hinzuzufügen.
  
### <a name="add-the-manage-credentials-command-to-the-quick-access-toolbar"></a>Hinzufügen des Befehls "Anmeldeinformationen verwalten" zur Symbolleiste für den Schnellzugriff

1.  Klicken Sie auf den Pfeil am rechten Ende der **Symbolleiste für den Schnellzugriff** , um das Menü **Symbolleiste für den Schnellzugriff anpassen** zu ziehen, und klicken Sie dann auf **Weitere Befehle**.
    
2. Wählen Sie in der Liste **Befehle auswählen** die Option **Alle Befehle** aus.
    
3. Verschieben Sie den Fensterinhalt der Liste nach unten zu **Anmeldeinformationen verwalten**, und klicken Sie dann auf **Hinzufügen**.
    
4. Klicken Sie auf **OK**.
    
Weitere Informationen zum Verwenden des Befehls **Anmeldeinformationen verwalten** und des Dialogfelds **Berechtigung** in InfoPath finden Sie im Thema zum Erstellen einer Formularvorlage mit eingeschränkter Berechtigung in der InfoPath-Hilfe. 
  
## <a name="the-irm-object-model"></a>Das IRM-Objektmodell

Verwenden Sie die [Permission](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.aspx) -Klasse, um auf die [UserPermissionCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermissionCollection.aspx) -und IRM-Berechtigungseinstellungen zuzugreifen, die auf ein Formular angewendet werden können. Verwenden Sie die [Permission](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Permission.aspx) -Eigenschaft der XmlForm-Klasse, um auf das **Berechtigungs** Objekt zuzugreifen, das einer Formularvorlage zugeordnet ist. [](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) Das zurückgegebene **Permission** -Objekt ermöglicht den Zugriff auf die Auflistung von [UserPermission](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermission.aspx) -Objekten, die der Formularvorlage und jeder Formularinstanz zugeordnet sind, die mit dieser Vorlage erstellt wurde. 
  
Das **Permission**-Objekt und seine Eigenschaften und Methoden sind unabhängig davon verfügbar, ob die Berechtigungen für die aktive Formularvorlage eingeschränkt sind oder nicht. Verwenden Sie die [Enabled](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.Enabled.aspx) -Eigenschaft, um zu bestimmen, ob ein Formular über eingeschränkte Berechtigungen verfügt. 
  
Berechtigungen für ein Formular werden auf eine der folgenden Arten mithilfe von Eigenschaften und Methoden der Permission-Klasse aktiviert:
  
Die **Enabled**-Eigenschaft ist auf **true** festgelegt.
  
Die [DocumentAuthor](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.DocumentAuthor.aspx) -Eigenschaft ist festgelegt. 
  
Die [RequestPermissionURL](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.RequestPermissionUrl.aspx) -Eigenschaft ist festgelegt. 
  
Die [StoreLicenses](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.StoreLicenses.aspx) -Eigenschaft ist auf **true** oder **false**festgelegt.
  
Die [ApplyPolicy](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.ApplyPolicy.aspx) -Methode wird aufgerufen. 
  
> [!NOTE]
> Wenn der Client für die Windows-Rechteverwaltung nicht auf einem Benutzercomputer installiert ist, löst die Verwendung der **Permission**-Klasse eine Ausnahme aus. 
  
Verwenden Sie die Klassen **UserPermissionCollection** und **UserPermission**, um programmgesteuert mit IRM-Einstellungen einzelner Benutzer in Formularen zu arbeiten. 
  
Ein **UserPermission**-Objekt ordnet eine Berechtigungsgruppe für das aktuelle Formular mit einem einzelnen Benutzer und einem optionalen Ablaufdatum zu. Verwenden Sie die [Add](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermissionCollection.Add.aspx) -Methode der **UserPermissionCollection** -Klasse, um einem Benutzer einen Satz von Berechtigungen für das aktuelle Formular hinzuzufügen und ihm zu gewähren. Verwenden Sie die [Remove](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermissionCollection.Remove.aspx) -Methode der **UserPermissionCollection** -Klasse, um einen Benutzer und die Berechtigungen des Benutzers zu entfernen. Während einige Berechtigungen, die über die Benutzeroberfläche gewährt werden, auf alle Benutzer angewendet werden, z. B. Drucken und Ablaufdatum, können Sie die Klassen **UserPermission** und **UserPermissionCollection** verwenden, um die Berechtigungen auf einer benutzerbezogenen Basis mit benutzerbezogenem Ablaufdatum zuzuweisen. Mithilfe des Objektmodells können Entwickler Berechtigungseinstellungen in einem Formular auflisten und Funktionalität bereitstellen, die Formularbenutzern ermöglicht, dem Formular Berechtigungen hinzuzufügen, ohne den Aufgabenbereich **Formularberechtigung** oder das Dialogfeld **Berechtigung** zu verwenden. 
  
> [!NOTE]
> Berechtigungen können nicht angewendet werden, wenn sich ein Formular im Vorschaumodus befindet. Aus diesem Grund sind alle Eigenschaften der **Permission**-Klasse schreibgeschützt, wenn die Vorschau für ein Formular angezeigt wird. Im Vorschaumodus gibt die **Enabled**-Eigenschaft immer **false** zurück, und wenn der Code versucht, diese Einstellung zu ändern, wird **System.Runtime.InteropServices.COMException** ausgelöst und der Fehler "Die Eigenschaft/Methode ist im Vorschaumodus nicht verfügbar" zurückgegeben. Auf ähnliche Weise geben die Methoden, die den Klassen **UserPermission** und **UserPermissionCollection** zugeordnet sind, diese Fehlermeldung zurück, wenn sie im Vorschaumodus verwendet werden. 
  
### <a name="overview-of-the-permission-class"></a>Übersicht über die "Permission"-Klasse

Die **UserPermissionCollection**-Klasse stellt die folgenden Eigenschaften und eine Methode bereit. 
  
|**Name**|**Beschreibung**|
|:-----|:-----|
|[ApplyPolicy](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.ApplyPolicy.aspx) -Methode  <br/> |Wendet eine Richtlinie auf das Formular mithilfe einer Richtlinienvorlagendatei an.  <br/> |
|[DocumentAuthor](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.DocumentAuthor.aspx) -Eigenschaft  <br/> |Ruft den Autor des aktuellen Formulars als e-Mail-Adresse ab oder legt ihn fest.  <br/> |
|[Enabled](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.Enabled.aspx) -Eigenschaft  <br/> |Ruft ab, ob die durch das **Permission**-Objekt dargestellten Berechtigungseinstellungen für das aktuelle Formular aktiviert sind, oder legt diese Einstellung fest.  <br/> |
|[PermissionFromPolicy](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.PermissionFromPolicy.aspx) -Eigenschaft  <br/> |Ruft ab, ob eine Berechtigungsrichtlinie auf dem aktuellen Formular angewendet wurde, oder legt diese Einstellung fest.  <br/> |
|[PolicyDescription](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.PolicyDescription.aspx) -Eigenschaft  <br/> |Ruft eine Beschreibung der Richtlinie ab, die auf dem aktuellen Formular angewendet wurde.   <br/> |
|[PolicyName](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.PolicyName.aspx) -Eigenschaft  <br/> |Ruft den Namen der Richtlinie ab, die auf dem aktuellen Formular angewendet wurde.  <br/> |
|[RequestPermissionURL](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.RequestPermissionUrl.aspx) -Eigenschaft  <br/> |Ruft die Datei, die URL oder die e-Mail-Adresse für Benutzer ab, die zusätzliche Berechtigungen für das aktuelle Formular benötigen, oder legt diese fest.  <br/> |
|[StoreLicenses](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.StoreLicenses.aspx) -Eigenschaft  <br/> |Ruft ab, ob die Benutzerlizenz zum Anzeigen des aktuellen Formulars zwischengespeichert werden soll, um die Offlineanzeige zuzulassen, wenn der Benutzer keine Verbindung zu einem Rechteverwaltungsserver herstellen kann, oder legt diese Einstellung fest.  <br/> |
|[UserPermissions](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.UserPermissions.aspx) -Eigenschaft  <br/> |Ruft ein **UserPermissionCollection**-Objekt für das aktuelle Formular ab.  <br/> |
   
### <a name="overview-of-the-userpermissioncollection-class"></a>Übersicht über die "UserPermissionCollection"-Klasse

Die **UserPermissionCollection**-Klasse stellt die folgenden Eigenschaften und Methoden bereit. 
  
|**Name**|**Beschreibung**|
|:-----|:-----|
|[Add](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermissionCollection.Add.aspx) -Methode (+ 3 Überladungen)  <br/> |Fügt dem aktuellen Formular einen neuen Benutzer hinzu; optional können Berechtigungen und ein Ablaufdatum angegeben werden.  <br/> |
|[Remove](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermissionCollection.Remove.aspx)-Methode  <br/> |Entfernt das **UserPermission**-Objekt mit dem angegebenen **UserId**-Objekt aus der Auflistung.  <br/> |
|[RemoveAll](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermissionCollection.RemoveAll.aspx) -Methode  <br/> |Entfernt alle **UserPermission**-Objekte aus der Auflistung.  <br/> |
|[Count](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermissionCollection.Count.aspx)-Eigenschaft  <br/> |Ruft die Anzahl der **UserPermission**-Objekte in der Auflistung ab.  <br/> |
|[Item](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermissionCollection.Item.aspx) -Eigenschaft (+ 1-Überladung)  <br/> |Ruft ein **UserPermission**-Objekt ab.  <br/> |
   
### <a name="overview-of-the-userpermission-class"></a>Übersicht über die "UserPermission"-Klasse

Die **UserPermission**-Klasse stellt die folgenden Eigenschaften und eine Methode bereit. 
  
|**Name**|**Beschreibung**|
|:-----|:-----|
|[Remove](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermission.Remove.aspx)-Methode  <br/> |Entfernt das aktuelle **UserPermission**-Objekt aus den Berechtigungen des Formulars.  <br/> |
|[ExpirationDate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermission.ExpirationDate.aspx) -Eigenschaft  <br/> |Ruft das optionale Ablaufdatum für die Berechtigungen auf dem aktuellen Formular ab, das dem Benutzer zugeordnet ist, der einer Instanz der **UserPermission**-Klasse zugeordnet ist, oder legt es fest.  <br/> |
|[Permission](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermission.Permission.aspx) -Eigenschaft  <br/> |Ruft einen Wert zur Darstellung der Berechtigungen auf dem aktuellen Formular ab, das dem Benutzer zugeordnet ist, der einer Instanz der **UserPermission**-Klasse zugeordnet ist, oder legt ihn fest.  <br/> |
|[UserID](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.UserPermission.UserId.aspx) -Eigenschaft  <br/> |Ruft die e-Mail-Adresse des Benutzers ab, dessen Berechtigungen für das aktuelle Formular vom angegebenen **UserPermission** -Objekt bestimmt werden.  <br/> |
   
### <a name="the-permissiontype-enumeration"></a>Die "PermissionType"-Enumeration

Die Berechtigungen eines Benutzers werden mit PermissionType- [](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.PermissionType.aspx) Enumerationswerten festgelegt oder gelesen. 
  
|**Name**|**Beschreibung**|
|:-----|:-----|
|**PermissionType. Change** <br/> |Ermöglicht Benutzern das Anzeigen, Bearbeiten, Kopieren und Speichern, jedoch nicht das Drucken eines Formulars. Entspricht einer Kombination der **Read**-, **Edit**-, **Save**- und **Extract**-Berechtigungen.  <br/> |
|**PermissionType. Edit** <br/> |Ermöglicht dem Benutzer das Bearbeiten des Formulars.  <br/> |
|**PermissionType. Extract** <br/> |Ermöglicht einem Benutzer, der über die **Read**-Berechtigung verfügt, das Kopieren der Formularinhalte.  <br/> |
|**PermissionType. FullControl** <br/> |Ermöglicht dem Benutzer das Hinzufügen, Ändern oder Entfernen von Berechtigungen für andere Benutzer eines Formulars.  <br/> |
|**PermissionType. objectModel** <br/> |Ermöglicht einem Benutzer über das zugehörige Objektmodell den programmgesteuerten Zugriff auf das Formulardokument. Benutzer, die nicht über die **ObjectModel**-Berechtigung verfügen, können das Objektmodell nicht verwenden, um ihre eigenen Berechtigungen festzulegen.  <br/> |
|**PermissionType. Print** <br/> |Ermöglicht dem Benutzer das Drucken des Formulars.  <br/> |
|**PermissionType. Read** <br/> |Ermöglicht dem Benutzer das Lesen (Anzeigen) des Formulars. (Die **Read**- und **View**-Berechtigungen sind äquivalent.)  <br/> |
|**PermissionType. Save** <br/> |Ermöglicht dem Benutzer das Speichern des Formulars.  <br/> |
|**PermissionType. View** <br/> |Ermöglicht dem Benutzer das Anzeigen (Lesen) des Formulars. (Die **Read**- und **View**-Berechtigungen sind äquivalent.)  <br/> |
   
### <a name="example"></a>Beispiel

Im folgenden Beispiel wird durch Klicken auf das Steuerelement **Schaltfläche** das **UserPermissionsCollection** für das aktuelle Formular abgerufen, ein Benutzer hinzugefügt und der Zugriffsebene Change zugewiesen und ein Ablaufdatum von zwei Tagen ab dem aktuellen Datum festgelegt. 
  
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


