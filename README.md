# Angular Material Form Design Project

This project demonstrates how to use Angular Material components to create a responsive and user-friendly form interface. The project features two main tabs: "Sign In" and "Sign Up," each with a form designed using Angular Material components.

## Features

- **Sign-In Form**: A simple form where users can enter their email and password to log in.
- **Sign-Up Form**: A form that allows users to create a new account by entering their personal details, such as first name, last name, age, gender, date of birth, and password.

## Technologies Used

- **Angular**: A platform for building robust web applications.
- **Angular Material**: A modern UI component library for Angular.
- **Reactive Forms**: A way to manage form controls with reactive programming.

## Code Overview

Here’s a quick overview of the code used in this project.

### HTML Structure

```html
<mat-tab-group mat-stretch-tabs>
  <!-- Sign In Tab -->
  <mat-tab label="Sign in">
    <form [formGroup]="signin" (ngSubmit)="signinSubmitted()">
      <mat-form-field appearance="outline">
        <mat-label>Email</mat-label>
        <input matInput placeholder="abxyz@gmail.com" formControlName="email" />
        <mat-error>Invalid Email</mat-error>
      </mat-form-field>

      <mat-form-field appearance="outline">
        <mat-label>Password</mat-label>
        <input matInput type="password" formControlName="password" />
        <mat-error>Invalid Password</mat-error>
      </mat-form-field>

      <button mat-raised-button color="primary">Login</button>
    </form>
  </mat-tab>

  <!-- Sign Up Tab -->
  <mat-tab label="Sign Up">
    <form [formGroup]="signup" (ngSubmit)="signupSubmitted()">
      <mat-form-field appearance="outline">
        <mat-label>First Name</mat-label>
        <input matInput placeholder="Alan" formControlName="firstName" />
        <mat-error>Required</mat-error>
      </mat-form-field>

      <mat-form-field appearance="outline">
        <mat-label>Last Name</mat-label>
        <input matInput placeholder="Zako" formControlName="lastName" />
        <mat-error>Required</mat-error>
      </mat-form-field>

      <mat-form-field appearance="outline">
        <mat-label>Age</mat-label>
        <input matInput placeholder="18" formControlName="age" />
        <mat-error>Required</mat-error>
      </mat-form-field>

      <!-- Gender Radio Buttons -->
      <mat-radio-group formControlName="gender">
        <mat-radio-button value="male">Male</mat-radio-button>
        <mat-radio-button value="female">Female</mat-radio-button>
      </mat-radio-group>

      <!-- Date of Birth Picker -->
      <mat-form-field appearance="outline">
        <mat-label>Date of Birth</mat-label>
        <input matInput [matDatepicker]="picker" formControlName="dob" />
        <mat-datepicker #picker></mat-datepicker>
      </mat-form-field>

      <mat-form-field appearance="outline">
        <mat-label>Password</mat-label>
        <input matInput type="password" formControlName="password" />
        <mat-error>Password is required</mat-error>
      </mat-form-field>

      <mat-form-field appearance="outline">
        <mat-label>Confirm Password</mat-label>
        <input matInput type="password" formControlName="confirmPassword" />
        <mat-error>Passwords must match</mat-error>
      </mat-form-field>

      <button mat-raised-button color="primary">Sign Up</button>
    </form>
  </mat-tab>
</mat-tab-group>
