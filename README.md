# Обновлено таблица перемешение
ALTER TABLE `i-man`.`history_per` 
ADD COLUMN `Users_ID` INT(11) NULL AFTER `toware`;
ALTER TABLE `i-man`.`history_per` 
ADD INDEX `UsersID` (`Users_ID` ASC);
  
# Добавлено новый таблица тип банка
CREATE TABLE `i-man`.`typebank` (
  `Id` INT NOT NULL AUTO_INCREMENT,
  `Name` VARCHAR(45) NULL,
  PRIMARY KEY (`Id`))
ENGINE = InnoDB
DEFAULT CHARACTER SET = utf8;
# Обновит таб Sales 
ALTER TABLE `i-man`.`sales` 
ADD COLUMN `Bank` INT(11) NULL DEFAULT NULL AFTER `clientdata`;
# Обновит таблица Users
ALTER TABLE `i-man`.`users` 
ADD COLUMN `Macaddress` VARCHAR(45) NULL AFTER `RoleId`;
# Добавит таблица Отчет по ревизия 
DROP TABLE IF EXISTS mdaftereditrevision;
CREATE TABLE mdaftereditrevision (
  ID int NOT NULL AUTO_INCREMENT,
  Sklad varchar(45) DEFAULT NULL,
  Namegoods varchar(255) DEFAULT NULL,
  D_srok datetime DEFAULT NULL,
  Price decimal(18,2) DEFAULT NULL,
  Summa decimal(18,2) DEFAULT NULL,
  Barcode varchar(255) DEFAULT NULL,
  AmountContainer int DEFAULT NULL,
  AmountUnit int DEFAULT NULL,
  UnitAmount int DEFAULT NULL,
  I_AmountContainer int DEFAULT NULL,
  I_AmountUnit int DEFAULT NULL,
  N_AmountContainer int DEFAULT NULL,
  N_AmountUnit int DEFAULT NULL,
  Polka varchar(128) DEFAULT NULL,
  Checked tinyint DEFAULT NULL,
  User varchar(45) DEFAULT NULL,
  Date_inserted datetime DEFAULT NULL,
  PRIMARY KEY (ID)
)
ENGINE = InnoDB AUTO_INCREMENT=1
DEFAULT CHARACTER SET = utf8;
 # I-man-files




